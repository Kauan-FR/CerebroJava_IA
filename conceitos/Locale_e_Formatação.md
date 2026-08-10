---
Data: 2026-08-10
tags:
  - java
  - conceito
  - formatacao
  - locale
cssclasses:
  - conceito
Fonte: raw/cursos/udemy/Java_COMPLETO_Programação_Orientada_a_Objetos_+_Projetos/teoria/Estrutura_Sequencial.pdf
---
## O que é

Um mesmo número tem apresentações diferentes conforme a região. `2100.0` vira `R$ 2.100,00` no Brasil e `$ 2,100.00` nos EUA. O valor é o mesmo; muda só como ele é exibido e lido. 

Em Java isso é representado pela classe `Locale`, passada como argumento em quem formata (`printf`) ou lê (`Scanner`).

## Por que importa

Formatação é **apresentação**, não domínio. Quando ela vira estado global, o programa passa a depender de onde está rodando. 

O sintoma é enganoso: o código funciona na sua máquina porque ela é brasileira, e quebra no servidor que roda em `en-US`. Nada no código mudou — mudou o ambiente. 

É por isso que container de produção fixa `LANG` e timezone explicitamente: para o comportamento não depender da máquina.