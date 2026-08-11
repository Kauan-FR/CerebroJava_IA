---
Data: 2026-08-10
tags:
  - java
  - conceito
  - imutabilidade
Tipo:
  - conceito
Fonte:
Paginas:
---
## O que é

A palavra-chave `final` impede que algo seja **substituído**. Em **variáveis**, impede apontar para outro objeto. Em **classe**, impede herdar. Em **método**, impede sobrescrever.
Em nenhum dos casos ele torna o objeto imutável. 
## Por que importa

O `final` é utilizado para que as classes elas se tornem seguras após a sua inicialização, pois por conta do `final` nenhuma outra classe pode derivar dela.

```java
private static final List<String> NOMES = new ArrayList<>();

NOMES = new ArrayList<>();   // erro de compilação
NOMES.add("Kauan");          // permitido
```

A lista é `final` e mudou de conteúdo.

O `final` ele protege a seta, ou seja, a reatribuição da variável, que no caso é o `new ArrayList<>()`, mas o objeto dentro da variável ela muda.

```java
private static final Locale PT_BR = Locale.of("pt", "BR");   // constante real
private static final Scanner SCANNER = new Scanner(System.in); // estado global mutável
```

`Locale` é imutável por dentro, então `final` basta para ele, já `Scanner` ele guarda a posição no buffer e muda a cada leitura.

## Como se aplica

```java
// Imutabilidade real exige que o objeto também seja imutável
public final class Money {
    private final BigDecimal amount;   // BigDecimal é imutável ✓
    private final Currency currency;
}

// Com coleção, final não basta
public final class Order {
    private final List<Item> items;    // ainda dá pra add/remove

    public List<Item> items() {
        return List.copyOf(items);     // devolve cópia imutável
    }
}
```

## Cuidado

- `final` em parâmetro de método impede reatribuir dentro do método. Em `main` é ruído
- Antes do Java 8, `final` era obrigatório pra usar variável em lambda. Hoje o compilador aceita _effectively final_
- `final` numa classe é o que garante o invariante de um value object: sem ele, alguém estende e sobrescreve o getter, contornando a validação do construtor

## Onde aparece

- [[Estado_Global]] - mutável + global é o que quebra

## Fontes