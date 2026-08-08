---
Data: 2026-08-08
Tags:
  - Exercício
Texto: Exercício do assunto Estrutura Sequencial
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/exercicio/Exercicios_Estrutura_Sequencial.pdf
---
---

```java
import java.util.InputMismatchException;  
import java.util.Scanner;  
  
public final class Exercicio_01 {  
  
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
        }catch (RuntimeException erro) {  
            throw new InputMismatchException("O valor informado não é um número válido.");  
        }  
    }  
}
```

## Observações das Escolhas

Eu utilizei o `try` com o `Scanner` porque como o `Scanner` ele é um valor mutável 