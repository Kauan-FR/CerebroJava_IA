---
Data: 2026-08-11
tags:
  - java
  - conceito
  - static
cssclasses:
  - conceito
Fonte:
Paginas:
---
## O que é 

A palavra-chave `static` é um modificador que indica que um membro ele pertence à classe em si, ou seja, só existe uma cópia desse membro na memória. Em **variáveis**, armazena dados comuns, como contadores globais. Em **métodos**, chama operações de forma direta. Em **classes**, não tem acesso de classes externas, tornado-se como classe independente.

## Por que importa

O `static` significa que o membro existe **antes e independente de qualquer objeto:**

```java
Math.sqrt(16);       // sem new Math()
Locale.of("pt","BR"); // sem new Locale()
```

## Como se aplica

## Cuidado

**Métodos estáticos não enxerga membro de instância** - porque não existe instância pra 

## Onde aparece
