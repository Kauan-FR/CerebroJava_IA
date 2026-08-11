---
Data: 2026-08-11
tags:
  - java
  - conceito
  - recursos
Tipo:
  - conceito
Fonte:
Paginas:
---
## O que é

Recurso é tudo aquilo que o sistema te empresta e espera receber de volta.
Se o sistema te emprestou uma conexão com o banco, você tem que devolvê-lo quando terminar - e é o `close()` que faz isso.

## Por que importa

O recurso é finito e emprestado, o sistema ele lhe empresta recursos como, uma conexão com o banco que tem um número fixo de conexões, um limite de arquivos abertos.

Acabar não devolvendo esse limite é *vazamento*. E o vazamento ele acaba aparecendo longe da sua causa original.

```java
Scanner sc = new Scanner(System.in);
int x = sc.nextInt();     // usuário digita "abc" → exceção aqui
sc.close();               // nunca executa
```

## Como se aplica

Usamos o **try-with-resources** para resolver esse problema:

```java
try (Scanner scanner = new Scanner(System.in)) {
    // usa
}   // fecha aqui — com sucesso, com exceção, com return
```

Com o uso do `try` teremos três garantias:

1. O fechamento é automático, em qualquer saída do bloco
2. Múltiplos recursos fecham na **ordem inversa** da abertura
3. Se o `close()` falhar, a exceção fica *suprimida* e anexada à original

## Cuidado

- **Fechar `System.in` é irreversível.** Depois disso, nenhum `Scanner` novo funciona. Em programa com menu, isso mata a aplicação
- **Não feche o que você não abriu.** Se um método recebe um `Scanner` pronto, ele não é o dono — quem criou fecha. Fechar recurso alheio quebra quem ainda ia usar
- **`static` + recurso** = recurso aberto pela vida inteira da aplicação, sem como fechar nem substituir em teste. Ver [[Estado_Global]]
- Existe um método `finalize()` que promete limpar sozinho. Está deprecated e nunca funcionou — não conte com ele

## Onde aparece

- [[Entrada_de_Dados]] - `Scanner` segurando `System.in`
- [[Ex_01_Estrutura_Sequencial]] - `close()` manual que não roda na aplicação
- [[Ex_01_V2_Estrutura_Sequencial]] - Tratamento de exceção com `catch`
- [[Estado_Global]] - `static Scanner`, recurso global sem dono
- [[Fronteira_de_Sistema]] - Recurso quase sempre vive na fronteira

## Fontes

