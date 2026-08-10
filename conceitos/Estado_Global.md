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

Em vez de guardar o valor num lugar alcançável por todo o programa, **passe-o como argumento** para que quem precisa dele. Quem chama decide; quem executa não depende de nada externo.
Guardar num `static final` só é seguro quando o objeto é imutável - `Locale` é, `Scanner` não é.

```java
// problema - o valor está num lugar que todo mundo alcança e pode mudar
Locale..setDefault(Locale.US);
System.out.printf("%.2f%n", price);

// solução - o valor chega pelo chamado
System.out.printf(Locale.US, "%.2f%n", price); 
```
## Cuidado

## Onde aparece

[[Saída_de_Dados]]
[[Entrada_de_Dados]]

## Fontes

[[Estrutura_Sequencial.pdf#page=15]]