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

É uma barreira onde reside a validação do sistema para que ele saiba que o que foi inserido é um objeto valido ou não.

## Por que importa

Como os objetos que entram de forma externa o sistema ele não tem pode de controlar, essa barreira ela é importante para barrar informações.

Sem essa barreira qualquer tipo de informação pode acessar o sistema.

## Como se aplica

Isso se aplica em três camada:

1. **Converte** - Texto para tipo;
2. **Valida formato** - É número? Tem os campos obrigatórios?
3. **Traduzir o erro** - Exceção técnica vira mensagem que o chamador entende

```java
private static int readInt(final Scanner scanner) {
    try {
        return scanner.nextInt();
    } catch (InputMismatchException e) {
        throw InvalidNumberInput.forValue(scanner.next(), e);
    }
}
```