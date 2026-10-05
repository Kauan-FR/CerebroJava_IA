---
Data: 2026-10-05
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Segundo a definição clássica de Inmon, um data warehouse é uma coleção de dados

(A) orientada a assunto, integrada, não volátil e variante no tempo, destinada ao apoio à decisão.
(B) orientada a transações, normalizada, volátil e atualizada em tempo real.
(C) temporária, utilizada exclusivamente durante o processo de carga.
(D) bruta, armazenada em formato original, sem qualquer transformação prévia.
(E) replicada de um sistema transacional, mantida idêntica à origem.

---

**2**

A característica de um data warehouse segundo a qual os dados são organizados em torno dos principais temas do negócio, como vendas, clientes ou produtos, é denominada

(A) orientação a assunto.
(B) integração.
(C) não volatilidade.
(D) variação no tempo.
(E) granularidade.

---

**3**

A característica de um data warehouse segundo a qual os dados, uma vez carregados, não são alterados nem excluídos pelos usuários, sendo apenas consultados, é denominada

(A) orientação a assunto.
(B) integração.
(C) não volatilidade.
(D) atomicidade.
(E) independência física.

---

**4**

Durante a carga de um data warehouse, constatou-se que o campo "sexo" era representado como "M/F" em um sistema de origem e como "1/2" em outro, exigindo padronização antes do armazenamento.

Essa necessidade decorre da característica de

(A) integração.
(B) não volatilidade.
(C) variação no tempo.
(D) orientação a assunto.
(E) volatilidade controlada.

---

**5**

A característica de um data warehouse segundo a qual os dados são armazenados com referência temporal, permitindo análises históricas e comparações entre períodos, é denominada

(A) orientação a assunto.
(B) integração.
(C) não volatilidade.
(D) variação no tempo.
(E) atualidade transacional.

---

**6**

Na abordagem proposta por Inmon, a construção do ambiente analítico parte

(A) do data warehouse corporativo, a partir do qual são derivados os data marts departamentais.
(B) dos data marts departamentais, posteriormente integrados por dimensões conformadas.
(C) do data lake, convertido progressivamente em cubos multidimensionais.
(D) dos sistemas transacionais, replicados integralmente sem transformação.
(E) das planilhas mantidas pelas áreas de negócio.

---

**7**

Na abordagem proposta por Kimball, a construção do ambiente analítico parte

(A) do data warehouse corporativo normalizado até a Terceira Forma Normal.
(B) dos data marts orientados a processos de negócio, integrados por meio de dimensões conformadas.
(C) do data lake com esquema aplicado na leitura.
(D) da replicação dos bancos transacionais em ambiente separado.
(E) da consolidação manual de relatórios departamentais.

---

**8**

Uma equipe disponibilizou, aos analistas, uma estrutura que reproduz parcialmente os dados operacionais com baixa latência, destinada a consultas operacionais integradas, sem o histórico profundo característico do ambiente analítico.

Essa estrutura é denominada

(A) data mart departamental.
(B) ODS (*operational data store*).
(C) cubo MOLAP pré-calculado.
(D) área de estágio do ETL.
(E) data lakehouse.

---

**9**

Uma diferença entre o data warehouse e os sistemas transacionais é que o data warehouse

(A) adota modelagem orientada à consulta analítica, com dados históricos consolidados, enquanto os sistemas transacionais são normalizados e voltados ao registro de operações correntes.
(B) adota modelagem normalizada voltada ao registro de operações, enquanto os sistemas transacionais são dimensionais.
(C) armazena apenas dados do dia corrente, enquanto os sistemas transacionais mantêm o histórico completo.
(D) dispensa processos de carga, por se conectar diretamente às origens.
(E) destina-se ao nível operacional, enquanto os sistemas transacionais atendem à alta direção.

---

**10**

O data warehouse apresenta características bem delimitadas.

**NÃO** constitui característica de um data warehouse a

(A) consolidação de dados provenientes de múltiplas fontes.
(B) manutenção de dados históricos para análise de tendências.
(C) atualização dos registros pelos usuários durante as consultas analíticas.
(D) organização dos dados em torno dos assuntos relevantes ao negócio.
(E) padronização de formatos e domínios durante o processo de carga.