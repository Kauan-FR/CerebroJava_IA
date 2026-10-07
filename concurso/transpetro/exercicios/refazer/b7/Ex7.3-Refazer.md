---
Data: 2026-10-07
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

O mapeamento de fontes de dados, em um projeto de Business Intelligence, consiste em

- [ ] (A) identificar e documentar quais sistemas e repositórios contêm os dados necessários, suas características e sua forma de acesso.
- [ ] (B) definir a estrutura física de armazenamento das tabelas de destino.
- [ ] (C) estabelecer o cronograma de implantação do data warehouse.
- [ ] (D) construir os relatórios e painéis que serão disponibilizados aos usuários.
- [ ] (E) controlar o acesso concorrente às transações nos sistemas transacionais.

---

**2**

Uma equipe registrou formalmente a correspondência entre cada coluna dos sistemas de origem e cada coluna das tabelas de destino, bem como as regras de transformação aplicadas a cada uma.

Essa documentação é denominada

- [ ] (A) mapeamento origem-destino (*source-to-target mapping*).
- [ ] (B) plano de execução do otimizador.
- [ ] (C) matriz de rastreabilidade de requisitos.
- [ ] (D) dicionário de dados do sistema operacional.
- [ ] (E) esquema conceitual normalizado.

---

**3**

Antes de iniciar a carga, uma equipe analisou o conteúdo efetivo das colunas de origem, verificando valores distintos, faixas, ocorrência de nulos e padrões de preenchimento.

Essa atividade é denominada

- [ ] (A) perfilamento de dados (*data profiling*).
- [ ] (B) modelagem dimensional.
- [ ] (C) particionamento horizontal.
- [ ] (D) normalização até a Terceira Forma Normal.
- [ ] (E) controle de concorrência pessimista.

---

**4**

Classificam-se como fontes internas de dados de uma organização

- [ ] (A) os sistemas transacionais, as planilhas departamentais e os bancos de dados corporativos.
- [ ] (B) os índices econômicos divulgados por institutos de pesquisa.
- [ ] (C) as bases de dados abertas mantidas por órgãos públicos.
- [ ] (D) as informações obtidas junto a fornecedores externos de dados.
- [ ] (E) os dados coletados em redes sociais de terceiros.

---

**5**

Durante o mapeamento, constatou-se que o mesmo cliente possui identificadores distintos em três sistemas de origem, sem chave comum entre eles.

O desafio caracterizado nessa situação é a

- [ ] (A) integração e reconciliação de identificadores entre as fontes.
- [ ] (B) violação da integridade de entidade do data warehouse.
- [ ] (C) ausência de granularidade definida para a tabela de fato.
- [ ] (D) necessidade de desnormalizar as tabelas de dimensão.
- [ ] (E) inadequação do nível de isolamento das transações.

---

**6**

Uma equipe precisa capturar, de forma incremental, apenas os registros alterados nos sistemas de origem desde a última carga, evitando a leitura integral das tabelas.

A técnica adequada a essa finalidade é

- [ ] (A) a captura de dados alterados (*change data capture*).
- [ ] (B) a replicação integral diária da base de origem.
- [ ] (C) o particionamento vertical das tabelas de destino.
- [ ] (D) a criação de índices sobre as colunas de origem.
- [ ] (E) a normalização prévia das fontes consultadas.

---

**7**

Ao mapear as fontes, a equipe registrou, para cada campo, sua origem, as transformações sofridas e os destinos em que é utilizado, permitindo rastrear o percurso completo do dado.

Esse registro corresponde à

- [ ] (A) linhagem de dados (*data lineage*).
- [ ] (B) política de retenção de dados.
- [ ] (C) matriz de responsabilidades do projeto.
- [ ] (D) estrutura analítica do projeto.
- [ ] (E) baseline de escopo aprovada.

---

**8**

Ao avaliar as fontes candidatas a alimentar o ambiente analítico, uma equipe deve considerar, entre outros aspectos,

- [ ] (A) a confiabilidade, a completude, a atualidade e a disponibilidade de acesso aos dados.
- [ ] (B) exclusivamente o volume de registros existente em cada fonte.
- [ ] (C) apenas a linguagem de programação utilizada no sistema de origem.
- [ ] (D) somente a quantidade de usuários cadastrados em cada sistema.
- [ ] (E) unicamente o fabricante do sistema gerenciador de banco de dados.

---

**9**

Durante o mapeamento, identificou-se que determinada informação está disponível tanto no sistema de faturamento quanto em uma planilha mantida pela área comercial, com divergências entre ambas.

A providência adequada consiste em

- [ ] (A) definir, junto às áreas de negócio, qual é a fonte autoritativa para aquela informação.
- [ ] (B) carregar as duas fontes simultaneamente, mantendo os valores divergentes.
- [ ] (C) descartar ambas as fontes e excluir a informação do escopo analítico.
- [ ] (D) adotar automaticamente a fonte com maior volume de registros.
- [ ] (E) converter a planilha em sistema transacional antes da carga.

---

**10**

O mapeamento de fontes de dados apresenta finalidades bem delimitadas.

**NÃO** constitui finalidade dessa atividade a

- [ ] (A) identificação dos sistemas que contêm os dados necessários ao projeto.
- [ ] (B) documentação das regras de transformação a serem aplicadas na carga.
- [ ] (C) avaliação da qualidade e da confiabilidade das fontes candidatas.
- [ ] (D) definição da identidade visual dos painéis disponibilizados aos usuários.
- [ ] (E) subsídio ao dimensionamento do esforço de integração necessário.