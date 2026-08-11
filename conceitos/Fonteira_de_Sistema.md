---
Data: 2026-08-11
tags:
  - conceito
  - arquitetura
  - validacao
cssclasses:
  - conceito
Fonte:
Paginas:
---
## O que é

É a linha onde o dado externo deixa de ser texto sem garantia e vira um tipo do sistema. Do lado de fora, tudo é texto; do lado de dentro, tudo tem tipo e regra.

## Por que importa

Como os objetos que entram de forma externa o sistema ele não tem pode de controlar, essa barreira ela é importante para barrar informações.

Sem essa barreira qualquer tipo de informação pode acessar o sistema.

## Como se aplica

Isso se aplica em três etapas:

1. **Converte** - Texto para tipo;
2. **Valida formato** - É número? Tem os campos obrigatórios?
3. **Traduzir o erro** - Exceção técnica vira mensagem que o chamador entende

```java
private static int readInt(final Scanner scanner) {
    try {
        return scanner.nextInt();
    } catch (InputMismatchException e) {
        throw InvalidNumberInput.forValue(scanner.next(), e);
    }
}
```

## Cuidado

Validar formato ≠ validar regra de negócio. 

- Fronteira: "consigo interpretar isso?" — é número, tem @, campo obrigatório presente 
- Domínio: "isso é permitido?" — saldo não pode ficar negativo, e-mail já cadastrado 
 
Regra de negócio na fronteira é regra que dá pra contornar: o job noturno, o script de importação e o outro endpoint não passam por ali. Invariante mora no domínio, porque é o único lugar por onde tudo passa.

## Onde aparece

- [[Entrada_de_Dados]] - `Scanner`, `InputMismatchException`, `useLocale`
- [[Ex_01_Estrutura_Sequencial]] - Hierarquia de exceção traduzindo erro de conversão
- [[Ex_01_V2_Estrutura_Sequencial]] - Traduzindo erro de exceção
- [[Estado_Global]] - `Locale` afeta como o dado externo é interpretado