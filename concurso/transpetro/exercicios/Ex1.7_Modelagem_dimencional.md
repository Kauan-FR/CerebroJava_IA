---
Data: 2026-08-27
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Na modelagem dimensional, a tabela que armazena as métricas quantitativas de um processo de negócio e as chaves que a ligam ao contexto analítico é denominada tabela

- [ ] (A) de dimensão.  
- [x] (B) de fato.  
- [ ] (C) associativa.  
- [ ] (D) temporária.  
- [ ] (E) de estágio.

---

**2**

Uma rede varejista modelou seu data warehouse com as tabelas a seguir.

```
Fato_Venda   (SK_Tempo, SK_Produto, SK_Loja, Quantidade, Valor_Total)
Dim_Tempo    (SK_Tempo, Data, Mes, Trimestre, Ano)
Dim_Produto  (SK_Produto, Descricao, Categoria, Departamento)
Dim_Loja     (SK_Loja, Nome, Cidade, Estado, Regiao)
```

Nesse modelo, as tabelas de dimensão

- [ ] (A) estão totalmente normalizadas até a Terceira Forma Normal.  
- [x] (B) encontram-se desnormalizadas, favorecendo o desempenho das consultas analíticas.  
- [ ] (C) armazenam exclusivamente medidas numéricas aditivas.  
- [ ] (D) possuem chave primária composta pelas chaves das demais dimensões.  
- [ ] (E) devem ser recriadas a cada carga do data warehouse.

---

**3**

Considere o modelo dimensional apresentado a seguir.

```
Fato_Venda ─── Dim_Produto ─── Dim_Categoria ─── Dim_Departamento
```

Nesse modelo, a dimensão Produto foi decomposta em tabelas adicionais normalizadas.

Esse tipo de estrutura caracteriza o esquema

- [ ] (A) estrela (star schema).  
- [x] (B) floco de neve (snowflake schema).  
- [ ] (C) constelação de fatos.  
- [ ] (D) relacional normalizado.  
- [ ] (E) em memória.

---

**4**

Uma equipe compara os esquemas estrela e floco de neve para o projeto de um data warehouse.

Uma vantagem do esquema estrela sobre o esquema floco de neve é

- [x] (A) a menor quantidade de junções necessárias nas consultas analíticas.  
- [ ] (B) a eliminação completa da redundância nas tabelas de dimensão.  
- [ ] (C) a ausência de tabelas de fato no modelo resultante.  
- [ ] (D) a impossibilidade de ocorrência de anomalias de atualização.  
- [ ] (E) o menor espaço total ocupado em disco pelas dimensões.

---

**5**

Durante o projeto de um data warehouse, a equipe definiu que cada tupla da tabela de fato representaria uma linha de item de um cupom fiscal, e não o total do cupom.

Essa definição corresponde à escolha

- [x] (A) da granularidade da tabela de fato.  
- [ ] (B) da cardinalidade das dimensões envolvidas.  
- [ ] (C) do tipo de dimensão de variação lenta.  
- [ ] (D) da estratégia de particionamento físico.  
- [ ] (E) do modelo de recuperação após falhas.

---

**6**

Em um data warehouse, uma tabela de fato foi definida com granularidade diária por produto e por loja. A área de negócio passou a exigir análises por hora de venda.

Nessa situação, o data warehouse

<font color="#ff0000">- [x] (A) atenderá à nova exigência sem qualquer alteração, por meio de operações de drill down.  </font>
<font color="#00b050">- [ ] (B) não conseguirá atender à nova exigência, pois o detalhe horário não foi armazenado.  </font>
- [ ] (C) atenderá à nova exigência mediante a criação de um índice sobre a coluna de data.  
- [ ] (D) atenderá à nova exigência mediante a normalização das tabelas de dimensão.  
- [ ] (E) não conseguirá atender à nova exigência, salvo se as dimensões forem desnormalizadas.

>[!fail] Granularidade é irreversível para baixo
>**Drill down só desce até onde o dado existe.** Se a tabela de fato guarda uma linha por dia, a informação de hora **não foi armazenada** — foi agregada e descartada na carga. Nenhuma operação OLAP recupera o que não está lá.
>O que se pode fazer com drill down é ir de ano → trimestre → mês → dia, porque tudo isso está contido no grão diário. De dia para hora, não: seria inventar dado.

---

**7**

Uma operadora de telefonia mantém, em seu data warehouse, a medida "saldo de linhas ativas", apurada ao final de cada mês.

Essa medida pode ser somada ao longo das dimensões produto e região, mas não pode ser somada ao longo da dimensão tempo.

Essa medida é classificada como

- [ ] (A) aditiva.  
- [x] (B) semiaditiva.  
- [ ] (C) não aditiva.  
- [ ] (D) derivada.  
- [ ] (E) degenerada.

---

**8**

Considere as medidas a seguir, mantidas na tabela de fato de um data warehouse comercial.

- Valor total da venda
- Percentual de margem de lucro

Essas medidas são classificadas, respectivamente, como

- [x] (A) aditiva e não aditiva.  
- [ ] (B) não aditiva e aditiva.  
- [ ] (C) semiaditiva e aditiva.  
- [ ] (D) aditiva e semiaditiva.  
- [ ] (E) não aditiva e semiaditiva.

---

**9**

Em um data warehouse, o número do cupom fiscal foi mantido na própria tabela de fato, sem que fosse criada uma tabela de dimensão específica para ele, uma vez que não possui atributos descritivos associados.

Esse atributo é classificado como dimensão

- [ ] (A) conformada.  
- [x] (B) degenerada.  
- [ ] (C) de variação lenta.  
- [ ] (D) papel (role-playing).  
- [ ] (E) lixo (junk).

---

**10**

Uma empresa de varejo alterou o endereço de um cliente em sua dimensão. A equipe optou por sobrescrever o valor antigo, mantendo apenas o dado atual, sem preservar o histórico.

Essa estratégia corresponde a uma dimensão de variação lenta (SCD) do tipo

- [ ] (A) 0  
- [x] (B) 1  
- [ ] (C) 2  
- [ ] (D) 3  
- [ ] (E) 4

---

**11**

Uma seguradora precisa analisar as vendas de seus corretores considerando a regional a que cada um pertencia **na data de cada venda**, e não a regional atual.

Para atender a esse requisito, a dimensão Corretor deve ser tratada como dimensão de variação lenta do tipo

- [ ] (A) 0, mantendo-se o valor original imutável.  
- [ ] (B) 1, sobrescrevendo-se o valor anterior.  
- [x] (C) 2, criando-se um novo registro a cada alteração, com chave substituta distinta.  
- [ ] (D) 3, mantendo-se apenas o valor atual e o imediatamente anterior em colunas separadas.  
- [ ] (E) 4, eliminando-se a dimensão e migrando-se seus atributos para a tabela de fato.

---

**12**

Em um data warehouse, adota-se o uso de chaves substitutas (surrogate keys) nas tabelas de dimensão.

Uma razão para essa adoção é

<font color="#00b050">- [ ] (A) permitir a coexistência de múltiplas versões históricas de um mesmo registro de origem.  </font>
<font color="#ff0000">- [x] (B) garantir a normalização das tabelas de dimensão até a Terceira Forma Normal.  </font>
- [ ] (C) eliminar a necessidade de tabelas de fato no modelo dimensional.  
- [ ] (D) reduzir a quantidade de dimensões necessárias ao modelo.  
- [ ] (E) assegurar que as medidas armazenadas sejam sempre aditivas.

>[!fail] Por que existe chave substituta no DW
>|SK_Corretor|ID_Corretor|Nome|Regional|Vigência|
>|---|---|---|---|---|
|1|3050|Ana|Nordeste|2024–2025|
>|2|3050|Ana|Sudeste|2026–|
>
>O `ID_Corretor` de origem é **3050 nas duas linhas**. Se ele fosse a chave primária, as duas versões não poderiam coexistir — a segunda violaria a unicidade. É a chave substituta (`SK_Corretor`) que permite as duas linhas existirem lado a lado, cada uma referenciada pelos fatos da época correspondente.
>Ou seja: **SCD tipo 2 é impossível sem surrogate key.** Uma coisa depende da outra.




---

**13**

Uma organização mantém as dimensões Tempo, Produto e Cliente compartilhadas, com a mesma estrutura e o mesmo conteúdo, por diferentes tabelas de fato de áreas distintas, permitindo análises integradas entre elas.

Essas dimensões são denominadas

- [ ] (A) degeneradas.  
- [x] (B) conformadas.  
- [ ] (C) lixo (junk).  
- [ ] (D) de variação lenta do tipo 3.  
- [ ] (E) papel (role-playing).

---

**14**

Em uma tabela de fato de pedidos, a dimensão Tempo é referenciada três vezes, por meio das chaves `SK_Data_Pedido`, `SK_Data_Faturamento` e `SK_Data_Entrega`.

Essa situação caracteriza uma dimensão

- [ ] (A) degenerada.  
- [x] (B) papel (role-playing).  
- [ ] (C) conformada.  
- [ ] (D) lixo (junk).  
- [ ] (E) de variação lenta do tipo 2.

---

**15**

Um analista executa, em uma ferramenta OLAP, a operação que parte da análise de vendas por ano e passa à análise por trimestre e, em seguida, por mês.

Essa operação é denominada

- [ ] (A) roll up.  
- [x] (B) drill down.  
- [ ] (C) slice.  
- [ ] (D) dice.  
- [ ] (E) pivot.

---

**16**

Em um cubo OLAP com as dimensões Tempo, Produto e Região, um analista fixa a dimensão Região no valor "Nordeste", obtendo um subcubo bidimensional composto pelas demais dimensões.

Essa operação é denominada

- [x] (A) slice.  
- [ ] (B) drill down.  
- [ ] (C) roll up.  
- [ ] (D) pivot.  
- [ ] (E) drill across.

---

**17**

Uma equipe implementa um ambiente OLAP em que os dados permanecem armazenados no banco de dados relacional, e as consultas multidimensionais são traduzidas em comandos SQL no momento da execução.

Essa arquitetura é classificada como

<font color="#ff0000">- [x] (A) MOLAP.  </font>
<font color="#00b050">- [ ] (B) ROLAP.  </font>
- [ ] (C) HOLAP.  
- [ ] (D) DOLAP.  
- [ ] (E) OLTP.

>[!fail] ROLAP x MOLAP
>|Arquitetura|Onde o dado fica|Consulta|
|---|---|---|
|**R**OLAP|Banco **R**elacional|traduzida em SQL na hora|
|**M**OLAP|Cubo **M**ultidimensional pré-calculado|leitura direta do cubo|
>|**H**OLAP|**H**íbrido: detalhe no relacional, agregados no cubo|conforme o nível|
>
>Trade-off que a banca cobra: MOLAP é mais rápido na consulta (tudo pré-calculado) mas exige processamento prévio e escala mal em volume. ROLAP escala melhor e reflete o dado atual, mas é mais lento porque calcula na hora.

---

**18**

Uma organização mantém um data warehouse corporativo e, a partir dele, disponibiliza subconjuntos departamentais voltados às áreas de vendas e de finanças.

Esses subconjuntos são denominados

- [ ] (A) data marts.  
- [x] (B) data lakes.  
- [ ] (C) áreas de estágio (staging areas).  
- [ ] (D) cubos degenerados.  
- [ ] (E) esquemas em floco de neve.

---

**19**

A modelagem dimensional apresenta características próprias, distintas das adotadas em ambientes transacionais.

**NÃO** constitui característica da modelagem dimensional a

- [ ] (A) desnormalização das tabelas de dimensão.  
- [ ] (B) orientação a processos de negócio analisáveis.  
- [ ] (C) definição explícita de granularidade da tabela de fato.  
- [x] (D) eliminação integral da redundância de dados armazenados.  
- [ ] (E) utilização de chaves substitutas nas dimensões.

---

**20**

Em um projeto de data warehouse, a equipe define os elementos que comporão a dimensão Tempo.

**NÃO** é atributo típico de uma dimensão Tempo a

- [ ] (A) indicação de dia útil ou não útil.  
- [ ] (B) identificação do trimestre e do semestre.  
- [ ] (C) marcação de feriado nacional.  
- [x] (D) quantidade total de itens vendidos no dia.  
- [ ] (E) identificação do dia da semana.