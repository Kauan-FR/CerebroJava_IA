---
Data: 2026-08-07
Tags:
  - Resumo
Texto: Resumo do assunto sobre Entrada de Dados em Java
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas: 22-28
---
|---

## O que é uma Entrada de Dados

É o processo onde de armazenamento de dados, registros e informações em um sistema computacional.

### Sintaxe

Para que ocorra uma entrada de dados na linguagem Java, é preciso que o código ele tenha a função a baixo:

```java
Scanner <nome> = new Scanner(System.in);
```

Para uma entrada do tipo texto ou char:

```java
String x = <nome do scanner>.next(); // Sem espaço
String y = <nome do scanner>.nextLine(); // Com espaço
char w = <nome do scanner>.next().charAt(0);
```

Para um entrada do tipo inteiro ou real:

```java
int x = <nome do scanner>.nextInt();
double y = <nome do scanner>.nextDouble();
float w = <nome do scanner>.nextFloat();
```

>[!warning] Atenção
>O `nextInt()` seguido do `nextLine()` ele pode não copilar direito, porque quando entrar com um número e apertar `Enter` o sistema pula a entrada do `String`, ficando no buffer.
>
>```java
>int idade = sc.nextInt();
>String nome = sc.nextLine(); // Vem vazio
>```
>
>Para evitar que isso aconteça colocamos um `nextLine()` vazio entre eles para que esse `nextLine()` ele consuma o `Enter` e assim consigamos entrar com o dado.
>
>```java
>int idade = sc.nextInt();
>sc.nextLine();
>String nome = sc.nextLine();
>```

## Fonte

[[Estrutura_Sequencial.pdf]] (p. 22-28)