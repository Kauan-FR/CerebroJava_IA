---
Data: 2026-08-11
tags:
  - java
  - conceito
  - static
cssclasses:
  - conceito
Fonte:
Paginas:
---
## O que é 

A palavra-chave `static` é um modificador que indica que um membro ele pertence à classe em si, ou seja, só existe uma cópia desse membro na memória. Em **variáveis**, armazena dados comuns, como contadores globais. Em **métodos**, chama operações de forma direta. Em **classes**, não tem acesso de classes externas, tornado-se como classe independente.

## Por que importa

O `static` significa que o membro existe **antes e independente de qualquer objeto:**

```java
Math.sqrt(16);       // sem new Math()
Locale.of("pt","BR"); // sem new Locale()
```

## Como se aplica

```java
// Legítimo — constante imutável de configuração
private static final Locale PT_BR = Locale.of("pt", "BR");

// Legítimo — utilitário sem estado
public final class StringUtils {
    private StringUtils() {}
    public static boolean isBlank(String s) { ... }
}

// Defeito — recurso mutável global
private static final Scanner SCANNER = new Scanner(System.in);
```

## Cuidado

**Métodos estáticos não enxerga membro de instância** - porque não existe instância pra enxergar:

```java
public class App {
    private int contador = 0;

    public static void main(String[] args) {
        contador++;   // erro: non-static variable in static context
    }
}
```

- Variável estática é **compartilhada por todo o programa**. Se for mutável, é estado global — ver [[Estado_Global]]
- Método estático não pode ser substituído em teste. Regra de negócio em método estático é regra que você não consegue testar isolada
- `static` em campo mutável, com múltiplas threads, é corrupção de dado

## Onde aparece
