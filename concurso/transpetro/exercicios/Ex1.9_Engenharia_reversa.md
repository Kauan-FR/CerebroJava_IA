---
Data: 2026-08-29
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Uma empresa assumiu a manutenção de um sistema em produção há doze anos, sem qualquer documentação de projeto, e precisa obter o modelo de dados correspondente ao banco existente.

O processo adequado a essa finalidade é denominado engenharia

- [x] (A) reversa.  
- [ ] (B) direta (forward).  
- [ ] (C) de requisitos.  
- [ ] (D) de desempenho.  
- [ ] (E) de dados mestres.

---

**2**

A engenharia reversa de banco de dados caracteriza-se por partir do modelo

- [ ] (A) conceitual em direção ao modelo físico.  
- [x] (B) físico em direção aos modelos lógico e conceitual.  
- [ ] (C) lógico em direção ao modelo físico.  
- [ ] (D) dimensional em direção ao modelo relacional.  
- [ ] (E) de requisitos em direção ao modelo conceitual.

---

**3**

Concluída a modelagem conceitual de um novo sistema, uma ferramenta CASE gerou automaticamente os comandos DDL de criação das tabelas no SGBD escolhido.

Esse processo é denominado engenharia

- [ ] (A) reversa.  
- [x] (B) direta (forward).  
- [ ] (C) de manutenção.  
- [ ] (D) de integração.  
- [ ] (E) de validação.

---

**4**

Uma equipe utiliza uma ferramenta que mantém o modelo de dados e o banco de dados sincronizados, permitindo tanto gerar o banco a partir do modelo quanto atualizar o modelo a partir de alterações realizadas diretamente no banco.

Esse recurso é denominado

- [ ] (A) engenharia reversa parcial.  
- [x] (B) round-trip engineering.  
- [ ] (C) normalização automática.  
- [ ] (D) replicação assíncrona.  
- [ ] (E) particionamento lógico.

---

**5**

Ao executar a engenharia reversa de um banco de dados relacional, uma ferramenta CASE obtém as estruturas das tabelas, colunas, tipos de dados e restrições declaradas.

A fonte primária dessas informações é

- [x] (A) o catálogo do sistema (dicionário de dados).  
- [ ] (B) o log de transações do SGBD.  
- [ ] (C) o conteúdo das tuplas armazenadas.  
- [ ] (D) o plano de execução gerado pelo otimizador.  
- [ ] (E) o código-fonte das aplicações que acessam o banco.

---

**6**

Durante a engenharia reversa de um sistema legado, constatou-se que nenhuma cláusula FOREIGN KEY havia sido declarada nas tabelas, embora as colunas de ligação existissem e fossem utilizadas pelas aplicações.

Nessa situação, a ferramenta de engenharia reversa

- [ ] (A) reconstruirá automaticamente todos os relacionamentos, com base nos valores armazenados.  
- [x] (B) não conseguirá inferir os relacionamentos a partir do catálogo, exigindo análise complementar de nomenclatura, dados e documentação.  
- [ ] (C) rejeitará a execução do processo, por ausência de integridade referencial.  
- [ ] (D) converterá automaticamente as colunas de ligação em chaves primárias compostas.  
- [ ] (E) obterá os relacionamentos a partir do log de transações do SGBD.

---

**7**

Após a engenharia reversa de um banco de dados legado, constatou-se que o modelo obtido apresentava tabelas com colunas repetidas e dependências transitivas não resolvidas.

Diante desse resultado, é correto afirmar que

- [ ] (A) a ferramenta executou o processo de forma incorreta, devendo ser substituída.  
- [x] (B) o modelo obtido reflete o banco existente, cabendo à equipe decidir sobre eventual normalização posterior.  
- [ ] (C) a engenharia reversa normaliza automaticamente as estruturas obtidas até a Terceira Forma Normal.  
- [ ] (D) o resultado indica que o banco de origem não possui chaves primárias definidas.  
- [ ] (E) o processo deve ser reexecutado a partir do modelo conceitual original.

---

**8**

Durante a engenharia reversa de um banco de dados, identificou-se a tabela a seguir.

```
AlunoDisciplina (ID_Aluno, ID_Disciplina, Nota)
   PRIMARY KEY (ID_Aluno, ID_Disciplina)
   FOREIGN KEY (ID_Aluno) REFERENCES Aluno(ID_Aluno)
   FOREIGN KEY (ID_Disciplina) REFERENCES Disciplina(ID_Disciplina)
```

No modelo conceitual reconstruído, essa tabela corresponde a

- [ ] (A) uma entidade fraca dependente de Aluno.  
- [x] (B) um relacionamento N:M entre Aluno e Disciplina, com atributo próprio.  
- [ ] (C) uma especialização da entidade Aluno.  
- [ ] (D) uma agregação entre Aluno e Disciplina.  
- [ ] (E) um relacionamento ternário entre Aluno, Disciplina e Nota.

---

**9**

Durante a engenharia reversa de um sistema de recursos humanos, identificou-se a tabela a seguir.

```
Empregado (Matricula, Nome, Matricula_Gerente)
   FOREIGN KEY (Matricula_Gerente) REFERENCES Empregado(Matricula)
```

No modelo conceitual reconstruído, essa estrutura corresponde a

- [ ] (A) um relacionamento ternário.  
- [x] (B) um autorrelacionamento na entidade Empregado.  
- [ ] (C) uma entidade fraca com relacionamento identificador.  
- [ ] (D) uma generalização com duas subclasses.  
- [ ] (E) uma dimensão de variação lenta do tipo 2.

---

**10**

Um banco de dados legado submetido a engenharia reversa possui tabelas denominadas `TB001`, `TB002` e `TB003`, com colunas nomeadas `C01`, `C02` e `C03`.

Em relação ao modelo obtido, é correto afirmar que ele

- [ ] (A) não poderá ser gerado, pois a ferramenta exige nomenclatura significativa.  
- [x] (B) reproduzirá a estrutura corretamente, mas com baixa expressividade semântica, exigindo interpretação complementar.  
- [ ] (C) atribuirá automaticamente nomes significativos, com base no conteúdo das colunas.  
- [ ] (D) violará a Primeira Forma Normal em razão da nomenclatura adotada.  
- [ ] (E) será equivalente a um modelo conceitual validado pelas áreas de negócio.

---

**11**

Uma equipe realizou a engenharia reversa de um banco de dados e obteve o modelo lógico correspondente. Constatou-se, porém, que determinadas regras de negócio implementadas exclusivamente no código das aplicações não foram representadas no modelo obtido.

Esse resultado ocorre porque a engenharia reversa de banco de dados

- [ ] (A) descarta deliberadamente as regras de negócio identificadas no catálogo.  
- [x] (B) recupera apenas o que está declarado nas estruturas do banco de dados.  
- [ ] (C) exige a execução prévia de um processo de normalização.  
- [ ] (D) depende da existência de um data warehouse corporativo.  
- [ ] (E) somente é aplicável a bancos de dados NoSQL.

---

**12**

Uma organização decidiu modernizar um sistema legado. Para isso, obteve o modelo de dados do banco existente, promoveu correções e melhorias nesse modelo e, em seguida, gerou o novo banco de dados a partir do modelo revisado.

Esse conjunto de atividades caracteriza um processo de

- [ ] (A) reengenharia.  
- [ ] (B) engenharia reversa exclusivamente.  
- [ ] (C) engenharia direta exclusivamente.  
- [ ] (D) desnormalização controlada.  
- [ ] (E) migração de dados mestres.

---

**13**

O modelo de dados mantido pela equipe de arquitetura encontra-se desatualizado em relação ao banco de dados em produção, no qual diversas alterações foram aplicadas diretamente ao longo do tempo.

O recurso adequado para identificar e incorporar essas diferenças ao modelo é a

(A) comparação e sincronização de esquemas (schema compare).  
(B) criação de índices sobre as tabelas alteradas.  
(C) execução de backup incremental do banco.  
(D) normalização das tabelas até a Forma Normal de Boyce-Codd.  
(E) definição de dimensões conformadas.

---

**14**

Durante a engenharia reversa de um banco de dados sem restrições declaradas, uma equipe analisou o conteúdo efetivamente armazenado nas colunas, verificando valores distintos, faixas de valores, ocorrência de nulos e padrões de formatação, a fim de inferir domínios e possíveis chaves.

Essa técnica é denominada

(A) perfilamento de dados (data profiling).  
(B) modelagem dimensional.  
(C) controle de concorrência otimista.  
(D) tuning de consultas.  
(E) mascaramento de dados.

---

**15**

Uma organização precisa migrar seu banco de dados de um SGBD para outro, de fabricante distinto.

Uma sequência adequada de atividades, do ponto de vista de modelagem, consiste em

(A) executar engenharia reversa do banco de origem, ajustar o modelo às características do SGBD de destino e executar engenharia direta.  
(B) executar engenharia direta no banco de origem e engenharia reversa no banco de destino.  
(C) copiar os arquivos físicos de dados do SGBD de origem para o de destino.  
(D) normalizar o banco de destino até a Terceira Forma Normal antes de qualquer análise.  
(E) executar o log de transações do banco de origem no SGBD de destino.

---

**16**

Durante a engenharia reversa de um banco de dados, identificaram-se as tabelas a seguir.

```
Pessoa        (ID_Pessoa, Nome, CPF)
PessoaFisica  (ID_Pessoa, Data_Nascimento)
                 PRIMARY KEY (ID_Pessoa)
                 FOREIGN KEY (ID_Pessoa) REFERENCES Pessoa(ID_Pessoa)
PessoaJuridica(ID_Pessoa, CNPJ, Razao_Social)
                 PRIMARY KEY (ID_Pessoa)
                 FOREIGN KEY (ID_Pessoa) REFERENCES Pessoa(ID_Pessoa)
```

No modelo conceitual reconstruído, essa estrutura indica

(A) um relacionamento N:M entre as três tabelas.  
(B) uma generalização/especialização, com Pessoa como superclasse.  
(C) três entidades independentes, sem relacionamento entre si.  
(D) uma agregação entre PessoaFisica e PessoaJuridica.  
(E) uma dimensão degenerada do modelo dimensional.

---

**17**

Uma equipe executou a engenharia reversa de um banco de dados NoSQL orientado a documentos, no qual não há esquema imposto pelo SGBD.

Nesse cenário, a obtenção da estrutura dos dados depende

(A) da consulta ao catálogo do sistema, que registra o esquema de cada coleção.  
(B) da análise dos documentos armazenados, inferindo-se campos, tipos e variações estruturais.  
(C) da leitura das restrições de integridade declaradas nas coleções.  
(D) da execução prévia da normalização das coleções até a Terceira Forma Normal.  
(E) da conversão obrigatória do banco para o modelo relacional.

---

**18**

Durante a engenharia reversa de um sistema de vendas, identificou-se a tabela `Pedido`, que contém as colunas `ID_Cliente`, `Nome_Cliente` e `Cidade_Cliente`, sendo que as duas últimas se repetem em todos os pedidos de um mesmo cliente.

A avaliação correta dessa estrutura, no modelo obtido, é que ela

(A) indica desnormalização existente no banco de origem, que deve ser avaliada pela equipe.  
(B) resulta de erro da ferramenta de engenharia reversa na leitura do catálogo.  
(C) caracteriza violação da integridade de entidade da tabela Pedido.  
(D) impede a reconstrução do relacionamento entre Pedido e Cliente.  
(E) demonstra que a tabela Pedido não possui chave primária definida.

---

**19**

A engenharia reversa de bancos de dados apresenta finalidades bem delimitadas.

**NÃO** constitui finalidade da engenharia reversa de banco de dados a

(A) documentação de sistemas legados sem modelo de dados disponível.  
(B) atualização de modelos desatualizados em relação ao ambiente em produção.  
(C) apoio à análise de impacto de alterações estruturais.  
(D) melhoria automática do desempenho das consultas executadas no banco.  
(E) obtenção de subsídios para processos de migração entre SGBDs.

---

**20**

Um analista listou informações que pretende obter por meio da engenharia reversa de um banco de dados relacional.

**NÃO** é obtida diretamente por esse processo a

(A) relação de tabelas e colunas existentes no banco.  
(B) definição dos tipos de dados de cada coluna.  
(C) intenção de negócio que motivou a criação de cada entidade.  
(D) relação de chaves primárias e estrangeiras declaradas.  
(E) relação de índices criados sobre as tabelas.