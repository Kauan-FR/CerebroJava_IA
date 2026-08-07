---
Data: 2026-08-06
Tags:
  - Estudo
Texto: Resumo sobre Variáveis e tipos primitivos em Java
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas: 4-7
---
---

## O que é uma Variável 

Em programação, variável é uma porção de memória que é utilizado para armazenado dados durante a execução de programas.

## Como se Declara uma Variável

Para que uma informação ela se torne uma variável, ela tem que ter as seguintes caracteristicas:
- Nome(ou um identificador da preferencia)
- Tipo
- Valor
- Endereço

### Sintaxe

```java 
<tipo> <nome> = <valor inicial>
```

> [!info] Observação
> O "valor inicial" ele pode ser qualquer valor, dês de que bata com o tipo presente e ela pode também não ter valor inicial

#### Exemplo

```java
int idade = 34;
double altura = 1.75;
char sexo = 'F';
String nome = "João Alves";
float salario = 1500f;  
```

### Tipos Primitivos em Java

|               Descrição               | Tipo    |
| :-----------------------------------: | ------- |
|       Tipos numéricos inteiros        | byte    |
|                                       | short   |
|                                       | int     |
|                                       | long    |
| Tipos numéricos com pontos flutuantes | float   |
|                                       | double  |
|         Um caractere Unicode          | char    |
|             Valor lógico              | boolean |
## Camel Case

O camel case são ou fazem parte das boas praticas de um programador, no caso do camel case é a formatação da escrita das variáveis que:
- Não pode começar com número, tem que começar ou com letra ou com `_`(anderline);
- Não pode conter espaços, preencha com `_`(anderline);

> [!info] Boas Praticas
> O java ele compila variáveis acentuadas, mas é considerado uma má prática, por conta disso que não se utiliza a pontuação em variáveis.

> [!failure] Errado
> ```java
> int 5minutos;
> int tempo de estudo;
> ```

>[!done] Correto
>```java
>int _5minutos;
>int tempoDeEstudo;
>```


## Fonte

[[Estrutura_Sequencial.pdf#page=4]] (p. 4-7)