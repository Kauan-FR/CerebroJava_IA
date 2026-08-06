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

```
System.out.print("Bom dia"); // Sem quebra de linha

System.out.println("Bom dia"); // Com quebra de linha
```

Essa sintaxe também é usada para receber valores de variáceis:

```
int y = 123;

System.out.println(y);
```

As variáveis com ponto flutuante são escritas dentro aspas duplas junto com o símbolo de porcentagem(%), da seguinte maneira:

```
double x = 10.123456

System.out.println("%.2f%n ", x);
```

> [!info] Informação
> O uso do "%n" é obrigatório sempre que a saída for dessa maneira, pois caso essa sigla não esteja

> [!info] Observação
> O número "2" ele pode ser quantos números o usuário quiser, ele representa a quantidade de casas decimais que o resultado terá.

