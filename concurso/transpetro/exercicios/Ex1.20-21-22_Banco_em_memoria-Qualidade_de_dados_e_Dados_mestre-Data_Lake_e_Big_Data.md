---
Data: 2026-09-07
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Um banco de dados em memória (_in-memory database_) caracteriza-se por

- [x] (A) manter os dados primariamente na memória principal, dispensando o acesso a disco durante as operações rotineiras.  
- [ ] (B) armazenar os dados exclusivamente em disco, utilizando memória apenas para o catálogo do sistema.  
- [ ] (C) eliminar a necessidade de qualquer mecanismo de recuperação após falhas.  
- [ ] (D) impedir a execução de transações com propriedades ACID.  
- [ ] (E) restringir-se ao armazenamento de dados não estruturados.

---

**2**

Uma equipe avalia a adoção de um banco de dados em memória para um sistema de negociação em tempo real.

A principal vantagem dessa tecnologia, nesse cenário, é

- [ ] (A) a redução do espaço total de armazenamento necessário.  
- [x] (B) a latência significativamente menor no acesso aos dados.  
- [ ] (C) a dispensa do uso de índices sobre as estruturas de dados.  
- [ ] (D) a eliminação da necessidade de modelagem de dados.  
- [ ] (E) a garantia automática de consistência eventual entre nós.

---

**3**

A principal limitação dos bancos de dados em memória, em comparação com os bancos tradicionais em disco, é

- [ ] (A) a impossibilidade de utilizar linguagem SQL para consultas.  
- [x] (B) a volatilidade da memória principal e o custo por unidade de armazenamento.  
- [ ] (C) a incapacidade de processar operações de escrita.  
- [ ] (D) a exigência obrigatória de modelagem dimensional.  
- [ ] (E) a ausência de suporte a controle de concorrência.

---

**4**

Para assegurar a durabilidade das transações, um banco de dados em memória utiliza, tipicamente,

- [ ] (A) exclusivamente a replicação de dados entre processos na mesma máquina.  
- [x] (B) a gravação de log de transações em armazenamento persistente e a geração periódica de _snapshots_.  
- [ ] (C) a recriação integral dos dados a partir das aplicações cliente após cada falha.  
- [ ] (D) a conversão automática do banco para o modelo dimensional.  
- [ ] (E) a desativação do controle de concorrência durante as escritas.

---

**5**

Uma organização utiliza uma solução em memória para armazenar temporariamente resultados de consultas frequentes, reduzindo a carga sobre o banco de dados principal.

Esse uso caracteriza a aplicação de

- [x] (A) cache.  
- [ ] (B) data lake.  
- [ ] (C) engenharia reversa.  
- [ ] (D) dimensão degenerada.  
- [ ] (E) particionamento vertical.

---

**6**

Na gestão da qualidade de dados, a dimensão que avalia se os dados armazenados correspondem à realidade que representam é a

- [x] (A) acurácia.  
- [ ] (B) completude.  
- [ ] (C) consistência.  
- [ ] (D) tempestividade.  
- [ ] (E) unicidade.

---

**7**

Uma organização identificou que 30% dos registros de clientes não possuem o campo de telefone preenchido.

A dimensão de qualidade de dados afetada nesse caso é a

- [ ] (A) acurácia.  
- [x] (B) completude.  
- [ ] (C) unicidade.  
- [ ] (D) conformidade.  
- [ ] (E) tempestividade.

---

**8**

Uma análise identificou que o mesmo cliente está cadastrado três vezes na base, com pequenas variações na grafia do nome.

A dimensão de qualidade de dados afetada é a

- [ ] (A) completude.  
- [x] (B) unicidade.  
- [ ] (C) tempestividade.  
- [ ] (D) acurácia.  
- [ ] (E) validade.

---

**9**

Em duas bases distintas de uma mesma organização, o campo "estado civil" apresenta o valor "C" em um sistema e "CASADO" em outro, para o mesmo indivíduo.

A dimensão de qualidade de dados afetada é a

- [x] (A) consistência.  
- [ ] (B) completude.  
- [ ] (C) tempestividade.  
- [ ] (D) unicidade.  
- [ ] (E) durabilidade.

---

**10**

Um relatório gerencial apresenta dados de vendas atualizados até três meses atrás, quando a área de negócio necessita de informações do dia anterior.

A dimensão de qualidade de dados afetada é a

(A) acurácia.  
(B) completude.  
(C) tempestividade (atualidade).  
(D) unicidade.  
(E) consistência.

---

**11**

Uma organização implantou um processo para identificar, consolidar e manter uma versão única e confiável dos dados de clientes, produtos e fornecedores, compartilhada por todos os sistemas corporativos.

Esse processo é denominado gestão de

(A) dados mestres (MDM).  
(B) transações distribuídas.  
(C) configuração de infraestrutura.  
(D) continuidade de negócios.  
(E) desempenho de consultas.

---

**12**

Em gestão de dados, a expressão "visão única do cliente" (_golden record_) refere-se

(A) ao registro consolidado que representa a versão mais confiável e completa de uma entidade, obtida a partir de múltiplas fontes.  
(B) ao backup diário dos dados cadastrais dos clientes.  
(C) ao índice criado sobre a chave primária da tabela de clientes.  
(D) à visão materializada que apresenta o total de vendas por cliente.  
(E) ao log de transações que registra as alterações no cadastro.

---

**13**

Um processo de qualidade de dados identifica registros que representam a mesma entidade do mundo real, ainda que apresentem grafias distintas, e os consolida em um único registro.

Esse processo é denominado

(A) deduplicação (_record matching_).  
(B) particionamento horizontal.  
(C) normalização até a Terceira Forma Normal.  
(D) engenharia reversa de dados.  
(E) controle de concorrência otimista.

---

**14**

Um data lake distingue-se de um data warehouse principalmente porque

(A) armazena dados brutos, em formato original, com esquema aplicado na leitura.  
(B) armazena exclusivamente dados estruturados previamente modelados.  
(C) exige modelagem dimensional antes da ingestão dos dados.  
(D) dispensa qualquer forma de catalogação ou governança.  
(E) substitui integralmente os sistemas transacionais da organização.

---

**15**

As características frequentemente associadas ao Big Data são conhecidas como os "V" do Big Data.

Os três "V" originalmente propostos são

(A) volume, velocidade e variedade.  
(B) volume, validade e visibilidade.  
(C) veracidade, valor e visualização.  
(D) velocidade, versionamento e volatilidade.  
(E) variedade, virtualização e vulnerabilidade.

---

**16**

Uma organização armazenou grande volume de arquivos em seu data lake sem catalogação, sem descrição de conteúdo e sem controle de origem. Os usuários passaram a não conseguir localizar nem confiar nos dados disponíveis.

Essa degradação caracteriza a formação de um(a)

(A) data mart departamental.  
(B) data swamp (pântano de dados).  
(C) esquema em floco de neve.  
(D) área de estágio do processo de ETL.  
(E) banco de dados em memória.

---

**17**

Uma arquitetura de dados moderna combina a flexibilidade de armazenamento de um data lake com recursos de gerenciamento de transações, governança e esquema típicos de um data warehouse.

Essa arquitetura é denominada

(A) data lakehouse.  
(B) data mart.  
(C) esquema estrela.  
(D) sistema OLTP distribuído.  
(E) banco de dados hierárquico.

---

**18**

Em um processo de integração de dados, uma organização adotou a abordagem em que os dados são extraídos das origens, carregados no repositório de destino em formato bruto e somente depois transformados, aproveitando a capacidade de processamento do próprio repositório.

Essa abordagem é denominada

(A) ETL.  
(B) ELT.  
(C) MDM.  
(D) OLAP.  
(E) CDC reverso.

---

**19**

A gestão da qualidade de dados envolve dimensões e práticas bem delimitadas.

**NÃO** constitui dimensão de qualidade de dados a

(A) acurácia dos valores armazenados.  
(B) completude dos campos obrigatórios.  
(C) consistência entre diferentes fontes.  
(D) quantidade de índices criados sobre as tabelas.  
(E) atualidade dos dados disponibilizados.

---

**20**

Um analista relacionou características atribuídas aos data lakes.

**NÃO** constitui característica de um data lake a

(A) armazenamento de dados estruturados, semiestruturados e não estruturados.  
(B) aplicação do esquema no momento da leitura.  
(C) custo de armazenamento geralmente inferior ao de um data warehouse.  
(D) exigência de modelagem dimensional prévia à ingestão dos dados.  
(E) utilização por cientistas de dados para exploração e análise avançada.