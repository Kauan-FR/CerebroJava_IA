---
Data: 2026-08-10
tags:
  - java
  - conceito
  - formatacao
  - locale
cssclasses:
  - conceito
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
---
## O que é

Um mesmo número tem apresentações diferentes conforme a região. `2100.0` vira `R$ 2.100,00` no Brasil e `$ 2,100.00` nos EUA. O valor é o mesmo; muda só como ele é exibido e lido. 

Em Java isso é representado pela classe `Locale`, passada como argumento em quem formata (`printf`) ou lê (`Scanner`).

## Por que importa

Formatação é **apresentação**, não domínio. Quando ela vira estado global, o programa passa a depender de onde está rodando. 

O sintoma é enganoso: o código funciona na sua máquina porque ela é brasileira, e quebra no servidor que roda em `en-US`. Nada no código mudou — mudou o ambiente. 

É por isso que container de produção fixa `LANG` e timezone explicitamente: para o comportamento não depender da máquina.

## Como se aplica

```java
// errado — muda a JVM inteira 
Locale.setDefault(Locale.US); 
System.out.printf("%.2f%n", price);

// certo — efeito limitado a esta linha 
System.out.printf(Locale.US, "%.2f%n", price);
```

Na leitura, o equivalente é `scanner.useLocale(Locale.US)`. 

Prova de que `setDefault` não serve: um programa que precisa exibir o mesmo valor em `pt-BR` e `en-US` na mesma execução é impossível com estado global. Com o Locale por chamada, é trivial.

## Cuidado

- `printf` respeita o Locale; `println` não. `println(10.5)` sempre imprime `10.5` 
- `Locale` é imutável — por isso funciona bem como `static final` 
- `new Locale(...)` está deprecated desde o Java 19. Use `Locale.of()`

## Onde aparece

[[Saida_de_Dados]] - `printf(Locale, ...)` e o marcador `%,.2f`
[[Entrada_de_Dados]] - `useLocale`, e o erro ao digitar `1.5` no Brasil
[[Estado_Global]] - o problema maio do qual este é um caso

## Fontes

[[Estrutura_Sequencial.pdf#page=15]]