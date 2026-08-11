---
Data: 2026-08-11
tags:
  - java
  - conceito
cssclasses:
  - conceito
Fonte:
Paginas:
---
## O que é

Exceção é um **objeto com tipo**. E tipo forma hierarquia, por conta disso que conseguimos capturar as exceções por hierarquias e não um por um.

```
Throwable
├── Error              → falha da JVM. Não capture.
└── Exception
    ├── (checked)      → obrigatório tratar ou declarar
    └── RuntimeException (unchecked)
```

|             | Checked                      | Unchecked                       |
| :---------: | ---------------------------- | ------------------------------- |
|   Exemplo   | `IOException`                | `IllegalArgumentException`      |
| Compilador  | Obriga tratar                | Não obriga                      |
| Quando usar | Falha esperada e recuperável | Erro de programação ou de regra |

## Por que importa

Sem essa hierarquia todas as exceções ficam sem um dono, consequentemente ficam espalhadas por aí, você acaba não conseguindo tratar por categoria:

```java
catch (InvalidNumberInput e) { ... }
catch (EmptyInput e) { ... }
catch (ValueOutOfRange e) { ... }   // e mais dez
```

Tendo uma exceção que será a base de todas as outras:

```java
catch (GlobalException e) { ... }
```

```java
DomainException      → 422
NotFoundException    → 404
ConflictException    → 409
```

Com isso conseguimos separar por categorias cada exceção.

## Como se aplica

**Base abstrata**, para ninguém instanciar a categoria:

```java
public abstract class GlobalException extends RuntimeException {
    protected GlobalException(final String message, final Throwable cause) {
        super(message, cause);
    }
}
```

**Filha final, com factory nomeada e construtor privado:**

```java
public final class InvalidNumberInput extends GlobalException {

    private InvalidNumberInput(final String message, final Throwable cause) {
        super(message, cause);
    }

    public static InvalidNumberInput forValue(final String value, final Throwable cause) {
        return new InvalidNumberInput("O valor '" + value + "' não é um número válido.", cause);
    }
}
```

Três decisões, três motivos:

- **Factory nomeada** - `forValue` diz o cenário. `new` com quatro parâmetros não diz nada
- **Construtor privado** - Força a passar pela factory, então a mensagem é sempre
- `final` - Ninguém estende e muda o significado

## Cuidado

- **Nunca perca a causa.** `throw new X("msg")` sem o `cause` apaga o stack trace. O log mostra onde você lançou, não onde quebrou
- **Não capture largo.** `catch (Exception)` ou `catch (RuntimeException)` engole NPE e erro de lógica seu, e converte tudo numa mensagem que mente
- **Exceção não é controle de fluxo.** Se acontece no caminho normal, é `if`, não `throw`. Exceção tem custo — ela monta o stack trace inteiro
- **Nunca engula:** `catch (E e) { }` vazio é o pior padrão que existe. O erro aconteceu e ninguém soube