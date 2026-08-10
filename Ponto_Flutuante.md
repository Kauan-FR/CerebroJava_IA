---
Data: 2026-08-10
tags:
  - java
  - conceito
  - precisao
Tipo:
  - conceito
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
Paginas:
---
## O que é

O binário ele não representa decimal exato em suas saídas, pois o problema fundamental é que números decimais comuns não tem representação exata em binário.

## Por que importa

```java
System.out.println(0.1 + 0.2);        // 0.30000000000000004
System.out.println(0.1 + 0.2 == 0.3); // false
```

Java tem dois jeitos de perder precisão: truncamento na divisão de inteiros, e representação binária em ponto flutuante. São causas diferentes.

```java
7 / 2       // 3    — divisão inteira, trunca
7.0 / 2     // 3.5
```

## Como se aplica

```java
// 1. Dinheiro → BigDecimal, sempre com String no construtor
BigDecimal valor = new BigDecimal("0.1");
BigDecimal outro = new BigDecimal(0.1);   // já entra errado

// 2. Comparação → tolerância, nunca ==
final double EPSILON = 0.000001;
if (Math.abs(a - b) < EPSILON) { ... }

// 3. Divisão de inteiros → força um dos lados a real
double media = (double) soma / quantidade;
```

## Cuidado

- `Math.pow(5, 2)` pode devolver `24.999...`. `(int)` trunca para 24 — use `Math.round()` quando quiser inteiro
- `float` tem ~7 dígitos confiáveis, `double` ~15. Use `double` sempre
- `printf("%.2f")` arredonda para exibir; o valor guardado continua errado
- `BigDecimal` compara com `compareTo()`, não `equals()` — `2.0` e `2.00` são iguais em valor e diferentes em `equals`
Nunca compare `double` com `==` é algo que parece que deveria funcionar, mas no fim da erro. Porque `0.1` em binário é uma dízima infinita, assim como o 1/3 é 0.333... em `double`. Cabe ate onde o `double` alcança, o restante se perde.

## Onde aparece

- [[Variaveis_e_Tipos_Primitivos_em_Java]] - `float` vs `double`, precisão
- [[Expressoes_Aritmeticas]] - divisão inteira 7/2
- [[Funcoes_Matematicas]] - `Math.pow` devolvendo 24.999
- [[Saida_de_Dados]] - `%.2f` arredonda a exibição, não o valor
## Fontes

- [[Estrutura_Sequencial.pdf]]