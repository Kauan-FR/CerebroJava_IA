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

## Como se aplica

## Cuidado

## Onde aparece

## Fontes