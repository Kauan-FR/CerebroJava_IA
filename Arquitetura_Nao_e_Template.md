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


