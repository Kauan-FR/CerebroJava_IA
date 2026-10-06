---
Data: 2026-10-06
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Na modelagem dimensional, a tabela que armazena as medidas quantitativas de um processo de negócio, juntamente com as chaves estrangeiras que a ligam ao contexto analítico, é a tabela

- [ ] (A) de dimensão.
- [x] (B) de fato.
- [ ] (C) associativa normalizada.
- [ ] (D) de estágio temporário.
- [ ] (E) de catálogo do sistema.

---

**2**

As tabelas de dimensão, em um esquema dimensional, caracterizam-se por

- [ ] (A) armazenar atributos descritivos que qualificam as medidas, sendo usualmente desnormalizadas.
- [ ] (B) conter exclusivamente medidas numéricas aditivas.
- [ ] (C) estar sempre normalizadas até a Forma Normal de Boyce-Codd.
- [ ] (D) possuir chave primária composta pelas chaves das demais dimensões.
- [ ] (E) ser recriadas integralmente a cada consulta analítica.

---

**3**

Um esquema dimensional em que as tabelas de dimensão se conectam diretamente à tabela de fato, sem decomposição em tabelas auxiliares, é denominado esquema

- [ ] (A) estrela.
- [ ] (B) floco de neve.
- [ ] (C) constelação normalizada.
- [ ] (D) relacional transacional.
- [ ] (E) hierárquico encadeado.

---

**4**

Uma equipe decompôs a dimensão Produto em tabelas adicionais de Categoria e Departamento, normalizando a hierarquia.

O esquema resultante é denominado

- [ ] (A) estrela.
- [ ] (B) floco de neve.
- [ ] (C) estrela degenerada.
- [ ] (D) dimensional plano.
- [ ] (E) multivalorado.

---

**5**

Um ambiente analítico possui várias tabelas de fato que compartilham as mesmas tabelas de dimensão, permitindo análises integradas entre diferentes processos de negócio.

Essa estrutura é denominada

- [ ] (A) esquema estrela isolado.
- [ ] (B) constelação de fatos.
- [ ] (C) floco de neve simples.
- [ ] (D) cubo degenerado.
- [ ] (E) área de estágio consolidada.

---

**6**

Em um projeto de data warehouse, a definição de que cada linha da tabela de fato representará um item de uma nota fiscal, e não o total da nota, corresponde à escolha

- [ ] (A) da granularidade da tabela de fato.
- [ ] (B) da estratégia de particionamento físico.
- [ ] (C) do tipo de dimensão de variação lenta.
- [ ] (D) da cardinalidade das dimensões envolvidas.
- [ ] (E) do nível de isolamento das consultas.

---

**7**

Uma medida pode ser somada ao longo das dimensões Produto e Loja, mas não pode ser somada ao longo da dimensão Tempo, por representar um saldo apurado ao final de cada período.

Essa medida é classificada como

- [ ] (A) aditiva.
- [ ] (B) semiaditiva.
- [ ] (C) não aditiva.
- [ ] (D) degenerada.
- [ ] (E) derivada.

---

**8**

O número do pedido foi mantido na própria tabela de fato, sem criação de tabela de dimensão específica, por não possuir atributos descritivos associados.

Esse atributo é classificado como dimensão

- [ ] (A) conformada.
- [ ] (B) degenerada.
- [ ] (C) lixo.
- [ ] (D) papel.
- [ ] (E) de variação lenta do tipo 1.

---

**9**

Uma seguradora precisa analisar o desempenho de seus corretores considerando a regional a que cada um pertencia na data de cada venda, e não a regional atual.

A dimensão Corretor deve ser tratada como dimensão de variação lenta do tipo

- [ ] (A) 0, mantendo-se o valor original inalterado.
- [ ] (B) 1, sobrescrevendo-se o valor anterior.
- [ ] (C) 2, criando-se novo registro a cada alteração, com chave substituta distinta.
- [ ] (D) 3, mantendo-se apenas o valor atual e o imediatamente anterior.
- [ ] (E) 4, migrando-se os atributos para a tabela de fato.

---

**10**

A modelagem dimensional apresenta características bem delimitadas.

**NÃO** constitui característica da modelagem dimensional a

- [ ] (A) desnormalização das tabelas de dimensão em favor do desempenho de consulta.
- [ ] (B) definição explícita da granularidade da tabela de fato.
- [ ] (C) utilização de chaves substitutas nas tabelas de dimensão.
- [ ] (D) eliminação integral da redundância entre os dados armazenados.
- [ ] (E) orientação a processos de negócio passíveis de análise.