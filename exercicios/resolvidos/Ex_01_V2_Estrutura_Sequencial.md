---
Data: 2026-08-09
tags:
  - java
  - exercicio
  - scanner
  - exception
Tipo:
  - exercicio
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/exercicio/Exercicios_Estrutura_Sequencial.pdf
Paginas: "1"
---
```java
public abstract class GlobalException extends RuntimeException {  
  
    protected GlobalException(final String message) {  
        super(message);  
    }  
  
    protected GlobalException(final String message,final Throwable cause) {  
        super(message, cause);  
    }  
}
```

```java
import exception.GlobalException;  
  
public final class InvalidNumberInput extends GlobalException {  
    private InvalidNumberInput(final String message, final Throwable cause) {  
        super(message,  cause);  
    }  
  
    public static InvalidNumberInput forValue(final String value, final Throwable cause) {  
        return new InvalidNumberInput(  
                "O valor '" + value + "' não é um número válido.", cause  
        );  
    }  
}
```

```java
import exercicios.Estrutura_Sequencial.Exercicio01.exception.InvalidNumberInput;  
  
import java.util.InputMismatchException;  
import java.util.Scanner;  
  
public final class IntSumExtracted {  
  
    static void main(String[] args) {  
  
        try (Scanner dado = new Scanner(System.in)){  
  
            System.out.println("Calculadóra Somatoria");  
            System.out.println();  
  
            final int first = rea(dado, "Entre com o primeiro valor: ");  
            final  int second = rea(dado, "Entre com o segundo valor: ");  
  
            System.out.printf("A soma de %d e %d é %d%n", first, second, first + second);  
        }  
    }  
  
    private static int rea(final Scanner dado, final String texto) {  
        System.out.print(texto);  
        try {  
            return dado.nextInt();  
        } catch (InputMismatchException e) {  
            throw InvalidNumberInput.forValue(dado.next(), e);  
        }  
    }  
}
```

## Observações das Escolhas

### Porque colocar `final` em tudo

O `final` ele é utilizado para que os parâmetros dentro do métodos não sejam reatribuídos. Sem ele qualquer outra classe pode reatribuir um valor a ela.