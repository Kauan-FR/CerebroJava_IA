---
Data: 2026-08-10
tags:
  - java
  - conceito
---
## O que é

É um dado que vive fora de qualquer escopo local e poder ser lido ou alterado de qualquer ponto do programa.

## Por que importa

Porque depende do ambiente, pois o programa ele pode funcionar na máquina pessoal, mas se o servidor estiver alocado em um local diferente o sistema ele quebra.
Os testes eles não funcionam de forma isolada, só localmente, e por conta disso o resultado ele passa a depender da ordem em que rodam.
Não da para ter dois valores.
## Como se aplica

Para que isso seja evitado, ao invés de declarar o valor isolado fora do escopo, declare ele dentro da variável, ou pode ate mesmo ao invés de escrever `Locale.US` atribua esse valor a uma varável para reduzir a sintaxe.

```java
public final Locale us = Locale.US;

System.out.printf(us, "%.2f%n", price);

// Ou direto na variavel
System.out.printf(Locale.US, "%.2f%n", price); 
```
## Cuidado

## Onde aparece

## Fontes