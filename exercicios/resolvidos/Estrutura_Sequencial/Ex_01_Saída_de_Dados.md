---
Data: 2026-08-07
Tags:
  - Exercício
Texto: Exercício de fixação sobre Saída de Dados
---
---

## Resposta

```java
import java.util.Locale;  
  
public class ExercicioFixacao {  
  
    private static final Locale PT_BR = Locale.forLanguageTag("pt-BR");  
    private static final Locale EN_US = Locale.US;  
  
    public static void main(String[] args) {  
  
        String produto1 = "Computador";  
        String produto2 = "Mesa de escritorio";  
          
        int anos = 30;  
        int codigo = 5290;  
        char genero = 'F';  
          
        double preco1 = 2100.0;  
        double prico2 = 1650.50;  
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

## Conceitos Aprendidos

### Locale: escopo local vs. estado global

O `Locale.setDefault()` muda a JVM inteira - afeta idiomas, moedas e ordenação de todo o programa. `printf(Locale, ...)` limita o efeito a uma linha.

> [!note] Sintoma
> Se o sistema funcionar mesmo que tenha algum bug sutil na sintaxe, é porque a maquina é brasileira, mas no final ela quebra no servidor.


## Observações

### Por que usar o `private static final` 

|  Palavra  | O que faz                              | Se tirar                            |
| :-------: | -------------------------------------- | ----------------------------------- |
| `private` | Esconde de **fora** da classe          | Outras classes passam a enxergar    |
| `static`  | Pertence a **classe**, não é um objeto | `main` não consegue mais usar       |
|  `final`  | Impede reatribuir                      | Qualquer método pode trocar o valor |
O `static` ele foi usado para que outros métodos estáticos consigam exergar, `private` para que nenhuma outra classe alcance, e `final` para que a referência não seja trocada.
Como `Local` é imutável por si só, isso resulta em constante de verdade.

## Fonte

[[Ex_Saída_de_Dados]]
[[Estrutura_Sequencial.pdf#page=15]]