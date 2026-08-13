---
Data: 2026-08-08
Tags:
  - java
  - exercicio
  - scanner
  - exception
Texto: Exercício do assunto Estrutura Sequencial
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/exercicio/Exercicios_Estrutura_Sequencial.pdf
Paginas: "1"
---
---

```java
import java.util.InputMismatchException;  
import java.util.Scanner;  
  
public final class IntSumInline {  
  
    static void main(String[] args) {  
  
        try (Scanner dado = new Scanner(System.in)) {  
  
            System.out.println("Calculadóra Somatoria");  
            System.out.println();  
            System.out.println("Entre com o primeiro valor:");  
            int valor1 = dado.nextInt();  
  
            System.out.println("Entre com o segundo valor:");  
            int valor2 = dado.nextInt();  
  
            int soma = valor1 + valor2;  
            System.out.printf("A soma do número %d e %d é %d", valor1, valor2, soma);  
        }catch (InputMismatchException erro) {  
            throw new InputMismatchException("O valor informado não é um número válido.");  
        }  
    }  
}
```

## Observações das Escolhas

### Porque utilizar o `try` ao invés do `sc.close()`

Esse `try` com o `Scanner` é um método chamado *try-with-resorces*.
O *try-with-resorces* ele é um método introduzido no Java 7 que automatiza o fechamento dos recursos externos, em outras palavras, ao invés de usar o `sc.close()` para fechar a classe, o `try` ele fecha automaticamente.

### Porque utilizar o `final` na classe

O `final` na nessa situação ele é desnecessário, mas ele é muito importante quando se trata de *Value Objects*, porque se o `final` ele não estiver na classe a subclasse ela pode anular a superclasse.

## Fonte

[[Exercicios_Estrutura_Sequencial.pdf]]



