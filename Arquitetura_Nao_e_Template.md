---
Data: 2026-08-11
tags:
  - java
  - conceito
  - arquitetura
Tipo:
  - conceito
Fonte:
Paginas:
---
## O que é

Arquitetura é o conjunto de decisões sobre **onde as fronteiras ficam** e **o que cada um protege.**
Cada camada existe para proteger algo específico — um invariante, uma regra que não pode ser violada, uma dependência que não pode vazar. Se não há nada a proteger, a camada não tem função.

O erro é tratar `domain/`, `repository/`, `entity/`, `event/` como estrutura que se copia de projeto em projeto. Isso produz pastas com nome de arquitetura e nada dentro que justifique existirem.

## Por que importa

Cada mudança, seja ela pequena que for tem que refletir nos cinco arquivos. Um campo novo vira alteração em entity, DTO, mapper, repository e service — sem nenhum ganho, porque não havia nada sendo protegido.


## Como se aplica

A pergunta que decide:

> **O que quebra se esta camada não existir?**

Se a resposta é concreta — "alguém cria `Quantia` com valor negativo", "a regra de cobrança vaza pro controller", "o domínio passa a depender do JPA" — a camada se justifica.

Se a resposta é "fica menos organizado" ou "não segue o padrão", não se justifica.

Consequência prática: **arquitetura cresce com o problema.** Começa com uma classe. Quando surge um invariante, nasce o value object. Quando o domínio começa a depender de infraestrutura, nasce a porta. Cada camada entra quando a pressão que ela alivia já existe — não antes.

## Cuidado

Isso não é desculpa para não pensar em arquitetura. Os dois erros custam caro:

|Erro|Sintoma|
|---|---|
|Estrutura demais cedo|Cinco camadas, zero regra de negócio|
|Estrutura de menos tarde|Regra de negócio espalhada em controller e service|

A diferença é _quando_. Estrutura antecipada você paga desde o dia um. Estrutura tardia você paga na refatoração — mas só se o projeto sobreviver até lá, e aí você já sabe qual estrutura precisa.

## Onde aparece

- [[Ex_01_Estrutura_Sequencial]] - Soma de dois inteiros não tem domínio
- [[Ex_01_V2_Estrutura_Sequencial]] - Também não tem domínio
- [[Estado_Global]] - Camada que vaza é camada que não protege
