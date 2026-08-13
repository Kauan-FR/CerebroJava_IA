---
Data: 2026-08-12
tags:
  - java
  - exercicio
Tipo:
  - exercicio
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/exercicio/Exercicios_Estrutura_Sequencial.pdf
---
Leia dois valores reais do teclado no formato brasileiro (`1234,56`) e exiba a soma com duas casas decimais e separador de milhar.

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
import java.util.Locale;  
import java.util.Scanner;  
  
public final class DecimalSumLocalized {  
  
    private static final Locale PT_BR = Locale.of("pt", "BR");  
  
    static void main(String[] args) {  
        try (Scanner dado = new Scanner(System.in)) {  
  
            dado.useLocale(PT_BR);  
  
            System.out.println("Calculadora");  
  
            final double firstNumber = read(dado, "Entre com o primero valor: ");  
            final double secondNumber = read(dado, "Entre com o segundo valor: ");  
  
            System.out.printf(PT_BR,"A soma de %,.2f e %,.2f é %,.2f%n",  firstNumber, secondNumber, firstNumber + secondNumber);  
        }  
    }  
  
    private static double read(final Scanner dado, final String label) {  
        System.out.print(label);  
  
        try {  
            return dado.nextDouble();  
        } catch (InputMismatchException e) {  
            throw InvalidNumberInput.forValue(dado.next(), e);  
        }  
    }  
}
```