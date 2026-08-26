---
Data: 2026-08-26
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Em um ambiente de gestão de dados corporativos, metadados são definidos como

- [ ] (A) os dados de maior volume armazenados no banco de dados.  
<font color="#00b050">- [x] (B) dados que descrevem características, estrutura e contexto de outros dados.  </font>
- [ ] (C) os dados replicados para fins de recuperação após falhas.  
- [ ] (D) os dados históricos mantidos exclusivamente em data warehouse.  
- [ ] (E) os registros de transações efetivadas em um período determinado.

---

**2**

Ao executar comandos de criação e alteração de tabelas, o SGBD registra automaticamente as informações sobre as estruturas criadas, tornando-as disponíveis para consulta.

Essas informações são armazenadas no(a)

- [ ] (A) log de transações.  
<font color="#00b050">- [x] (B) catálogo do sistema, também denominado dicionário de dados.  </font>
- [ ] (C) plano de execução gerado pelo otimizador.  
- [ ] (D) área de buffer de memória do SGBD.  
- [ ] (E) conjunto de arquivos de backup incremental.

---

**3**

Em um Sistema Gerenciador de Banco de Dados (SGBD) relacional, um repositório de metadados armazena informações sobre os dados que estão armazenados no banco de dados propriamente dito, auxiliando desenvolvedores e administradores a compreender e a gerenciar o ambiente.

Dentre as informações típicas encontradas nos metadados de um banco de dados relacional, está(ão)

- [ ] (A) o faturamento total apurado pelas transações do período.  
- [ ] (B) as senhas dos usuários e suas permissões no sistema operacional.  
<font color="#ff0000">- [x] (C) o código-fonte das aplicações que acessam o banco de dados.  </font>
- [ ] (D) as cópias de segurança dos dados armazenados nas tabelas.  
<font color="#00b050">- [ ] (E) os esquemas das tabelas, incluindo os tipos de dados de suas colunas.</font>

>[!fail] O que guarda no metadado
>A questão ela pedia para dizer o que se encontra nos metadados.
>**O padrão desta questão, que vale para todas as de metadados:** as quatro alternativas erradas descrevem **dado, conteúdo ou artefato externo** — faturamento, senhas de SO, código-fonte, backup. Só uma descreve **estrutura**. Metadado é sempre estrutura, nunca conteúdo.

---

**4**

Considere as informações a seguir, registradas em um repositório corporativo de metadados.

- Definição do termo "Cliente Ativo" aprovada pela área de negócio
- Responsável (data owner) pelo domínio de dados de vendas
- Regra de negócio aplicada ao cálculo do indicador de inadimplência

Essas informações são classificadas como metadados

- [ ] (A) técnicos.  
- [ ] (B) operacionais.  
<font color="#00b050">- [x] (C) de negócio.  </font>
- [ ] (D) estruturais.  
- [ ] (E) físicos.

---

**5**

Considere as informações a seguir, extraídas do catálogo de um banco de dados relacional.

- Nome e tipo de dado de cada coluna
- Chaves primárias e estrangeiras declaradas
- Índices existentes sobre cada tabela

Essas informações são classificadas como metadados

- [ ] (A) de negócio.  
<font color="#00b050">- [x] (B) técnicos.  </font>
- [ ] (C) operacionais.  
- [ ] (D) semânticos.  
- [ ] (E) transacionais.

---

**6**

Uma equipe de governança registra, para cada carga do data warehouse, a data e a hora de execução, o volume de registros processados e a quantidade de erros ocorridos.

Essas informações constituem metadados

- [ ] (A) de negócio.  
- [ ] (B) técnicos.  
<font color="#00b050">- [x] (C) operacionais.  </font>
- [ ] (D) conceituais.  
- [ ] (E) dimensionais.

---

**7**

Um analista precisa consultar, por meio de comandos SQL padronizados, a relação de tabelas e colunas existentes em determinado banco de dados relacional.

Para essa finalidade, ele deve consultar

<font color="#00b050">- [x] (A) as visões do INFORMATION_SCHEMA.  </font>
- [ ] (B) o arquivo de log de transações.  
- [ ] (C) o plano de execução das consultas.  
- [ ] (D) os arquivos de dump gerados pelo backup.  
- [ ] (E) as tabelas de fato do data warehouse.

---

**8**

Uma equipe de dados necessita identificar a origem de determinado indicador exibido em um painel gerencial, percorrendo todas as transformações sofridas pelo dado desde o sistema transacional de origem.

O recurso de metadados adequado a essa finalidade é a(o)

<font color="#00b050">- [x] (A) linhagem de dados (data lineage).  </font>
- [ ] (B) modelagem dimensional.  
- [ ] (C) particionamento horizontal.  
- [ ] (D) controle de concorrência.  
- [ ] (E) plano de recuperação de desastres.

---

**9**

Antes de alterar o tipo de dado de uma coluna em um sistema de origem, uma equipe precisa identificar todos os relatórios, painéis e processos de carga que serão afetados por essa mudança.

O procedimento apoiado pelos metadados, nesse caso, é a análise de

<font color="#00b050">- [x] (A) impacto.  </font>
- [ ] (B) requisitos.  
- [ ] (C) desempenho.  
- [ ] (D) viabilidade.  
- [ ] (E) concorrência.

---

**10**

Uma consultoria recebeu apenas o acesso a um banco de dados em produção, sem qualquer documentação, e precisa obter o modelo de dados correspondente.

Nesse processo, as ferramentas de engenharia reversa obtêm as estruturas das tabelas a partir

<font color="#00b050">- [x] (A) dos metadados registrados no catálogo do sistema.  </font>
- [ ] (B) dos registros do log de transações.  
- [ ] (C) das estatísticas coletadas pelo otimizador.  
- [ ] (D) do conteúdo das tuplas armazenadas nas tabelas.  
- [ ] (E) dos arquivos de configuração do sistema operacional.

---

**11**

Uma organização implantou um repositório de metadados corporativo.

**NÃO** constitui benefício esperado dessa implantação a

- [ ] (A) padronização da terminologia utilizada pelas áreas de negócio.  
- [ ] (B) identificação da origem e das transformações aplicadas aos dados.  
<font color="#ff0000">- [x] (C) redução do tempo necessário para localizar informações relevantes.  </font>
<font color="#00b050">- [ ] (D) eliminação da necessidade de realizar cópias de segurança dos dados.  </font>
- [ ] (E) apoio à análise de impacto de alterações nas estruturas de dados.

>[!fail] Questão negativa
>Metadados descrevem dados; não os protegem. Backup continua obrigatório, sem qualquer relação com catalogação

---

**12**

Em um processo de ETL de um data warehouse, registra-se formalmente a correspondência entre cada coluna dos sistemas de origem e cada coluna das tabelas de destino, bem como as regras de transformação aplicadas.

Essa documentação constitui um conjunto de metadados denominado

<font color="#00b050">- [x] (A) mapeamento origem-destino (source-to-target mapping).  </font>
- [ ] (B) plano de execução do otimizador.  
- [ ] (C) esquema em floco de neve.  
- [ ] (D) política de retenção de dados.  
- [ ] (E) matriz de responsabilidades do projeto.

---

**13**

Uma organização armazenou grande volume de arquivos em um data lake, sem catalogação, sem descrição de conteúdo e sem controle de origem. Com o tempo, os usuários passaram a não conseguir localizar nem confiar nos dados disponíveis.

Essa degradação, decorrente da ausência de metadados, caracteriza a formação de um(a)

- [ ] (A) data mart.  
<font color="#00b050">- [x] (B) data swamp (pântano de dados).  </font>
- [ ] (C) data warehouse corporativo.  
- [ ] (D) banco de dados em memória.  
- [ ] (E) esquema estrela.

---

**14**

Uma empresa precisa assegurar que o termo "receita líquida" tenha significado único e padronizado em todos os relatórios corporativos, independentemente da área que o utilize.

O instrumento de gestão de metadados adequado a essa finalidade é o(a)

<font color="#00b050">- [x] (A) glossário de negócio.  </font>
- [ ] (B) dicionário de dados técnico.  
- [ ] (C) log de auditoria.  
- [ ] (D) plano de capacidade.  
- [ ] (E) matriz de riscos.

---

**15**

Para atender às exigências da Lei Geral de Proteção de Dados Pessoais, uma organização precisa identificar, em todo o seu ambiente, quais colunas armazenam dados pessoais e quais armazenam dados pessoais sensíveis.

O recurso que viabiliza esse levantamento de forma sistemática é

<font color="#00b050">- [x] (A) a classificação de dados registrada nos metadados.  </font>
- [ ] (B) o particionamento das tabelas por faixa de datas.  
- [ ] (C) a criação de índices sobre as colunas envolvidas.  
- [ ] (D) a compactação dos arquivos de dados.  
- [ ] (E) a replicação síncrona entre os servidores.

---

**16**

Considere a execução do comando a seguir em um banco de dados relacional.

sql

```sql
ALTER TABLE Cliente ADD email VARCHAR(80);
```

Em relação aos metadados do banco, essa execução

- [ ] (A) não produz qualquer efeito, pois apenas dados são alterados.  
<font color="#00b050">- [x] (B) atualiza automaticamente o catálogo do sistema com a nova coluna.  </font>
- [ ] (C) exige a atualização manual do catálogo pelo administrador.  
- [ ] (D) atualiza automaticamente o modelo conceitual mantido pela equipe.  
- [ ] (E) invalida todos os metadados previamente registrados na tabela.

---

**17**

Uma equipe diferencia os conceitos utilizados em seu ambiente de dados.

Na tabela `Venda`, o registro do valor R$ 1.500,00 na coluna `valor_total`, definida como DECIMAL(10,2), constitui

- [ ] (A) um metadado, e a definição DECIMAL(10,2) constitui um dado.  
<font color="#00b050">- [x] (B) um dado, e a definição DECIMAL(10,2) constitui um metadado.  </font>
- [ ] (C) um metadado, assim como a definição DECIMAL(10,2).  
- [ ] (D) um dado, assim como a definição DECIMAL(10,2).  
- [ ] (E) uma informação derivada, sem relação com metadados.

---

**18**

Uma organização implantou uma ferramenta de catálogo de dados corporativo, que permite às áreas de negócio pesquisar quais conjuntos de dados existem, quem é o responsável por cada um e qual o seu nível de confiabilidade.

A principal finalidade dessa ferramenta é

- [ ] (A) executar as cargas de dados entre os ambientes.  
<font color="#00b050">- [x] (B) promover a descoberta e a compreensão dos ativos de dados existentes.  </font>
- [ ] (C) substituir o sistema gerenciador de banco de dados relacional.  
- [ ] (D) realizar o backup e a recuperação dos dados armazenados.  
- [ ] (E) controlar a concorrência entre transações simultâneas.

---

**19**

Em bancos de dados NoSQL orientados a documentos, adota-se com frequência a abordagem de esquema flexível (schema-on-read).

Nesse contexto, em comparação com os bancos relacionais, os metadados de estrutura

<font color="#ff0000">- [x] (A) deixam de existir, pois não há qualquer estrutura definida.  </font>
- [ ] (B) são registrados exclusivamente no log de transações.  
<font color="#00b050">- [ ] (C) não são impostos previamente pelo SGBD, cabendo à aplicação interpretá-los na leitura.  </font>
- [ ] (D) são obrigatoriamente declarados antes da inserção de qualquer documento.  
- [ ] (E) tornam-se idênticos aos metadados de um data warehouse dimensional.

>[!fail] NoSQL e schema-on-read
>Campos, tipos, aninhamento — isso é estrutura. O que muda é **quem impõe e quando:**
>
>||Quando o esquema é validado|Quem valida|
|---|---|---|
|**Schema-on-write** (relacional)|Na **gravação** — a linha é rejeitada se não bater|O **SGBD**|
|**Schema-on-read** (documento)|Na **leitura** — o documento entra do jeito que vier|A **aplicação**|

---

**20**

Um administrador consulta o catálogo do sistema para obter informações de apoio à sua rotina de trabalho.

**NÃO** é obtida por meio da consulta ao catálogo do sistema a

- [ ] (A) relação de índices existentes sobre determinada tabela.  
- [ ] (B) definição das restrições de integridade declaradas.  
<font color="#ff0000">- [x] (C) relação de privilégios concedidos a cada usuário do banco.  </font>
- [ ] (D) quantidade de tuplas efetivamente armazenadas em cada tabela.  
<font color="#00b050">- [ ] (E) sequência de operações executadas por uma transação específica.</font>

>[!fail] Questão negativa
>
>
>A resposta é (E): **a sequência de operações executadas por uma transação específica**. Isso está no **log de transações**, não no catálogo.
>
>||Guarda|Natureza|
|---|---|---|
|**Catálogo**|Tabelas, colunas, tipos, índices, restrições, visões, privilégios, estatísticas|**Estrutura** — permanente|
|**Log de transações**|Sequência de operações, valores antes/depois, marcas de commit|**Histórico** — cronológico|