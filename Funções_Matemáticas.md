---
Data: 2026-08-07
Tags:
  - Estudo
Texto: Resumo do assunto sobre Funções Matemáticas em Java
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas: 28-30
---
---

## O que são Funções Matemáticas

É a relação entre dois conjuntos onde cada elemento do primeiro está associado a um único elemento do segundo.

## Em Java

As funções matemáticas em Java são escritas da seguinte maneira:

| Exemplo              | Significado                                                |
| :------------------- | ---------------------------------------------------------- |
| `A = Math.sqrt(x)`   | Raiz quadrada. A varável `A` recebe a raiz quadrada de `x` |
| `A = Math.pow(x, y)` | Potenciação. `A` recebe o resultado de `x` elevado a `y`   |
| `A = Math.abs(x)`    | Valor absoluto. `A` recebe o valor absoluto de `x`         |

## Sintaxe

Para tirar a raiz quadrada de um valor:

```java
A = Math.sqrt(25.0);
System.out.println("Raiz quadrada de 25 = " + A);
```

Para elevar um valor a potencia:

```java
A = Math.pow(5.0, 2.0);
System.out.println("5 elevado ao quadrado = " + C);
```

Para extrair o valor absoluto de um valor:

```java
double x = 4.0;
A = Math.abs(x);
System.out.println("Valor absoluto de " + x + " = " + A);
```

## Fonte

[[Estrutura_Sequencial.pdf]] (p. 28-30)