---
Data: 2026-08-07
Tags:
  - Exercício
  - Resolvido
Texto: Exercício de fixação sobre Saída de Dados
---
---

## Resposta

```java
import java.util.Locale;  
  
public class ExercicioFixacao {  
  
    private static final Locale PT_BR = Locale.forLanguageTag("pt-BR");  
    private static final Locale EN_US = Locale.US;  
  
    static void main(String[] args) {  
  
        String produto1 = "Computador";  
        String produto2 = "Mesa de escritorio";  
          
        int anos = 30;  
        int codigo = 5290;  
        char genero = 'F';  
          
        double preco1 = 2100.0;  
        double price2 = 1650.50;  
        double medida = 53.234567;  
  
        System.out.println("Produtos na moeda Brasileira:");  
        System.out.printf(PT_BR,"%s, o valor dele é R$ %,.2f%n", produto1, preco1);  
        System.out.printf(PT_BR,"%s, o valor dela é R$ %,.2f%n", produto2, price2);  
  
        System.out.printf("%n");  
        System.out.println("Produtos na moeda US");  
        System.out.printf(EN_US,"%s, o valor dele é $ %,.2f%n", produto1, preco1);  
        System.out.printf(EN_US,"%s, o valor dela é $ %,.2f%n", produto2, price2);  
  
        System.out.printf("%n");  
        System.out.printf("Registro, %d anos, codigo %d e genero: %c%n", anos, codigo, genero);  
  
        System.out.printf("%n");  
        System.out.printf(PT_BR,"Meça com oito casas decimais: %.8f%n", medida);  
        System.out.printf(EN_US, "US pontos decimais:  %.3f%n", medida);  
    }  
}
```

## Observações

### Por que usar o `private static final` 

|  Palavra  | O que faz                              | Se tirar                            |
| :-------: | -------------------------------------- | ----------------------------------- |
| `private` | Esconde de **fora** da classe          | Outras classes passam a enxergar    |
| `static`  | Pertence a **classe**, não é um objeto | `main` não consegue mais usar       |
|  `final`  | Impede reatribuir                      | Qualquer método pode trocar o valor |
