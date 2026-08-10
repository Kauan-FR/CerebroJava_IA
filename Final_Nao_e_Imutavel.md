---
Data: 2026-08-10
tags:
  - java
  - conceito
Tipo:
  - conceito
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
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
## Como se aplica

## Cuidado

## Onde aparece

## Fontes