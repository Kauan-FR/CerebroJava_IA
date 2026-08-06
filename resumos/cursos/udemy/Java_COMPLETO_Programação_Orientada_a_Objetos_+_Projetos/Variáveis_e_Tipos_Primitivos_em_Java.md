---
Data: 2026-08-06
Tags:
  - Estudo
Texto: Resumo sobre Variáveis e tipos primitivos em Java
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

```
<tipo> <nome> = <valor inicial>
```

> [!info] Observação
> O "valor inicial" ele pode ser qualquer valor, dês de que bata com o tipo presente e ela pode também não ter valor inicial

#### Exemplo

```
int idade = 34;
double altura = 1.75;
char sexo = 'F';
String nome = "João Alves";  
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
|           Valor verdadeiro            | boolean |
## Camel Case

O camel case são ou fazem parte das boas praticas de um programador, no caso do camel case é a formatação da escrita das variáveis que:
- Não pode começar com número, tem que começar ou com letra ou com `_`(anderline);
- Não pode conter espaços, preencha com `_`(anderline);
- Não pode ter acentuação.

> [!failure] Errado
> ```
> int 5minutos;
> int tempo de estudo;
> int salário;
> ```

>[!todo] Correto
>```
>int _5minutos;
>int tempo_de_estudo;
>int salario;
>```

## Fonte

[[Estrutura_Sequencial.pdf#page=4]] (p. 4-7)