---
Data: 2026-08-10
tags:
  - conceito
  - arquitetura
  - design
cssclasses:
  - conceito
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas:
---
## O que é

Cada fato do sistema tem **um único lugar** onde ele é definido. Todo o resto deriva dele.

Quando o mesmo fato existe em dois lugares, eles podem divergir - e o sistema acaba não sabendo entre as duas respostas a qual vale.

## Por que importa

Por definirmos o resultado em uma variável, e não deixarmos o sistema definir o resultado, caso venhamos a alterar o enunciado, o resultado ele passa a ser mentiroso, pois a base ela foi alterada, mas como o resultado ele esta pré definido na variável, o resultado ele não acompanha, acabando sendo um resultado mentiroso que o sistema ele não aponta.

```java
double unit1 = 2100.0;
int quant1 = 2;
double total1 = 4200.0;   // terceiro fato, derivado dos outros dois
```

## Como se aplica

```java
// duas fontes de verdade
final double total = 4200.0;

// uma fonte, o resto deriva
final double total = quantidade * precoUnitario;
```

## Cuidado

Cache é duplicidade deliberada, você aceita a duplicidade, mas assume obrigação de invalidar.

**Camadas diferentes representam o mesmo fato de propósito.** Um DTO de resposta repete campos da entidade — e isso é certo, porque desacopla a API do banco. A diferença: existe um dono claro, e a cópia é gerada a partir dele.

## Fontes

- [[Estrutura_Sequencial.pdf]]