---
Data: 2026-08-07
Tags:
  - java
  - resumo
  - matematica
Texto: Resumo do assunto sobre Funções Matemáticas em Java
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas: 28-30
---
---

## O que são Funções Matemáticas em Java

`Math` é uma classe utilitária de `java.lang` com métodos **estáticos** para operações matemáticas. Chama-se pela classe (`Math.sqrt(x)`), sem criar objeto.

As funções matemáticas em Java são escritas da seguinte maneira:

| Exemplo              | Significado                                                |
| :------------------- | ---------------------------------------------------------- |
| `A = Math.sqrt(x)`   | Raiz quadrada. A varável `A` recebe a raiz quadrada de `x` |
| `A = Math.pow(x, y)` | Potenciação. `A` recebe o resultado de `x` elevado a `y`   |
| `A = Math.abs(x)`    | Valor absoluto. `A` recebe o valor absoluto de `x`         |

## Sintaxe

Para tirar a raiz quadrada de um valor:

```java
double A;
A = Math.sqrt(25.0);
System.out.println("Raiz quadrada de 25 = " + A);
```

Para elevar um valor a potencia:

```java
double A;
A = Math.pow(5.0, 2.0);
System.out.println("5 elevado ao quadrado = " + A);
```

Para extrair o valor absoluto de um valor:

```java
double A;
A = Math.abs(4.0);
System.out.println("Valor absoluto de 4.0 é = " + A);
```

## Fonte

[[Estrutura_Sequencial.pdf]] (p. 28-30)