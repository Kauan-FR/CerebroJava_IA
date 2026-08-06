---
Data: 2026-08-06
Tags:
  - Estudo
Texto: Resumo sobre Saída de dados em Java
Fonte: raw/cursos/java/teoria/Estrutura_Sequencial.pdf
Paginas: 10-16
---
---

## O que é Saída de Dados

É o processo que uma maquina leva para transferir informações processadas, exibindo o resultado por meio de uma tela, impressão, reprodução de vídeo ou som.

### Sintaxe

A sintaxe de uma saída de dados em java é:

```java
System.out.print("Bom dia"); // Sem quebra de linha

System.out.println("Bom dia"); // Com quebra de linha
```

##### Essa sintaxe também é usada para receber valores de variáveis:

```java
int y = 123;

System.out.println(y);
```

As variáveis com ponto flutuante são escritas dentro aspas duplas junto com o símbolo de porcentagem(%), da seguinte maneira:

```java
double x = 10.123456

System.out.printf("%.2f%n ", x);
```

> [!info] Informação
> O uso do "%n" é obrigatório para que ocorra uma quebra de linha, pois para essa saída de dados utilizamos o `printf` ao invés do `println` 

> [!info] Observação
> O número "2" ele pode ser quantos números o usuário quiser, ele representa a quantidade de casas decimais que será arredondadas no resultado final.


Uma outra forma de adicionar o valor de uma variável a saída é utilizando a expressão +(mais) para concatenação, dessa maneira:

```java
int x = 10

System.out.println("O Eduardo tem " + x + " anos de idade");
```

Agora para juntar vários elementos em uma única saída é assim:

```java
String nome = "Eduardo";
int idade = 10;
double renda = 100.0;

System.out.printf("%s com %d de idade, recebe um valor de %.2f por mês de messada", nome, idade, renda) 
```

A tabela para referenciar essa estrutura é:

| Sigla | Significado           |
| :---: | --------------------- |
| `%f`  | Para valores reais    |
| `%d`  | Para valores inteiros |
| `%s`  | Para texto            |
| `%n`  | Quebra de linha       |

## Pergunta 

`printf` e `println` fazem a mesma coisa quando você não vai formatar nada. Então **por que o `printf` existe?**

O `printf` ele existe para controlar o formato do valor da saída. E acaba se tornando mais legível a utilização dele para concatenar vários elementos.
Já o `println` ele só despeja o valor na tela.