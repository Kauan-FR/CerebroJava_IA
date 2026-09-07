---
Data: 2026-09-06
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Em um Sistema Gerenciador de Banco de Dados (SGBD), a independência de dados física caracteriza-se por permitir que

- [ ] (A) alterações no esquema conceitual não afetem as aplicações existentes.  
- [x] (B) alterações na forma de armazenamento não afetem o esquema conceitual nem as aplicações.  
- [ ] (C) as chaves estrangeiras sejam declaradas sem tabela referenciada.  
- [ ] (D) as transações sejam executadas sem controle de concorrência.  
- [ ] (E) os metadados sejam armazenados fora do catálogo do sistema.

---

**2**

Uma das funções essenciais de um SGBD é assegurar que, após a confirmação de uma transação, seus efeitos persistam mesmo diante de falha de energia ou queda do servidor.

O recurso utilizado pelo SGBD para viabilizar essa garantia é o(a)

- [ ] (A) log de transações.  
- [x] (B) catálogo do sistema.  
- [ ] (C) plano de execução do otimizador.  
- [ ] (D) índice composto sobre a chave primária.  
- [ ] (E) área de estágio do processo de ETL.

---

**3**

Uma transação bancária transfere R$ 500,00 da conta A para a conta B, executando um débito e um crédito. Ocorre falha após o débito e antes do crédito, e o SGBD desfaz integralmente a operação.

A propriedade ACID que assegura esse comportamento é a

- [x] (A) atomicidade.  
- [ ] (B) consistência.  
- [ ] (C) isolamento.  
- [ ] (D) durabilidade.  
- [ ] (E) concorrência.

---

**4**

Duas transações simultâneas acessam a mesma tabela. O SGBD assegura que cada uma seja executada como se fosse a única em execução, sem que os resultados intermediários de uma sejam visíveis à outra.

A propriedade ACID correspondente é a

- [ ] (A) atomicidade.  
- [ ] (B) consistência.  
- [x] (C) isolamento.  
- [ ] (D) durabilidade.  
- [ ] (E) integridade referencial.

---

**5**

As propriedades ACID são fundamentais para garantir a confiabilidade das transações em um Sistema Gerenciador de Banco de Dados Relacional.

A descrição correta das quatro propriedades ACID é:

- [ ] (A) Atomicidade: o banco permanece em estado válido após a transação. Consistência: a transação é executada integralmente ou não é executada. Isolamento: os efeitos da transação são permanentes. Durabilidade: transações simultâneas não interferem entre si.

- [x] (B) Atomicidade: a transação é executada integralmente ou não é executada. Consistência: o banco permanece em estado válido, respeitando as restrições definidas. Isolamento: transações simultâneas não interferem entre si. Durabilidade: os efeitos da transação confirmada são permanentes.

- [ ] (C) Atomicidade: transações simultâneas não interferem entre si. Consistência: a transação é dividida em subtransações menores. Isolamento: o banco permanece em estado válido. Durabilidade: a transação é executada integralmente ou não é executada.

- [ ] (D) Atomicidade: os efeitos da transação confirmada são permanentes. Consistência: transações simultâneas não interferem entre si. Isolamento: a transação é executada integralmente ou não é executada. Durabilidade: o banco permanece em estado válido.

- [ ] (E) Atomicidade: a transação é dividida em subtransações menores. Consistência: os efeitos da transação são permanentes. Isolamento: o banco permanece em estado válido. Durabilidade: transações simultâneas não interferem entre si.

---

**6**

Os comandos `COMMIT`, `ROLLBACK` e `SAVEPOINT` pertencem à

- [ ] (A) Linguagem de Definição de Dados (DDL).  
- [ ] (B) Linguagem de Manipulação de Dados (DML).  
- [ ] (C) Linguagem de Controle de Dados (DCL).  
- [x] (D) Linguagem de Controle de Transações (TCL).  
- [ ] (E) Linguagem de consulta multidimensional.

---

**7**

Uma transação T1 alterou o salário de um empregado e ainda não confirmou a operação. Nesse intervalo, a transação T2 leu o novo valor. Em seguida, T1 executou `ROLLBACK`.

O problema de concorrência caracterizado nessa situação é a

- [ ] (A) leitura suja (dirty read).  
- [ ] (B) leitura não repetível (non-repeatable read).  
- [x] (C) leitura fantasma (phantom read).  
- [ ] (D) perda de atualização (lost update).  
- [ ] (E) escrita suja (dirty write).

---

**8**

Uma transação T1 executou uma consulta que retornou 20 linhas. Em seguida, a transação T2 inseriu novas linhas que satisfazem a mesma condição e confirmou a operação. Ao reexecutar a mesma consulta, T1 obteve 23 linhas.

O problema de concorrência caracterizado nessa situação é a

- [x] (A) leitura suja.  
- [ ] (B) leitura não repetível.  
- [ ] (C) leitura fantasma.  
- [ ] (D) perda de atualização.  
- [ ] (E) violação de atomicidade.

---

**9**

Um analista precisa configurar o nível de isolamento que impede a ocorrência de leitura suja, mas ainda admite leitura não repetível.

O nível de isolamento adequado é

- [ ] (A) READ UNCOMMITTED.  
- [ ] (B) READ COMMITTED.  
- [x] (C) REPEATABLE READ.  
- [ ] (D) SERIALIZABLE.  
- [ ] (E) SNAPSHOT ISOLATION.

---

**10**

Em relação aos níveis de isolamento definidos pelo padrão SQL, é correto afirmar que o nível

- [ ] (A) READ UNCOMMITTED oferece o maior grau de isolamento e o menor desempenho.  
- [x] (B) SERIALIZABLE oferece o maior grau de isolamento e o maior custo de concorrência.  
- [ ] (C) READ COMMITTED impede a ocorrência de leitura fantasma.  
- [ ] (D) REPEATABLE READ permite a ocorrência de leitura suja.  
- [ ] (E) SERIALIZABLE dispensa o uso do log de transações.

---

**11**

Bancos de dados NoSQL classificam-se em diferentes categorias, conforme o modelo de dados adotado.

O banco de dados que armazena entidades e as relações entre elas como estruturas de primeira classe, sendo especialmente adequado a análises de redes sociais e detecção de fraudes, é o orientado a

- [ ] (A) chave-valor.  
- [x] (B) documentos.  
- [ ] (C) colunas (família de colunas).  
- [ ] (D) grafos.  
- [ ] (E) objetos relacionais.

---

**12**

Uma aplicação precisa armazenar sessões de usuários, com acesso extremamente rápido a partir de um identificador único, sem necessidade de consultas por outros atributos.

O tipo de banco NoSQL mais adequado a esse requisito é o orientado a

- [x] (A) chave-valor.  
- [ ] (B) documentos.  
- [ ] (C) grafos.  
- [ ] (D) colunas.  
- [ ] (E) relacional normalizado.

---

**13**

Uma equipe optou por um banco de dados NoSQL orientado a documentos para armazenar cadastros com estruturas variáveis entre si.

Uma característica desse tipo de banco é

- [x] (A) exigir a definição prévia de esquema fixo para todas as coleções.  
- [ ] (B) permitir que documentos de uma mesma coleção possuam campos distintos entre si.  
- [ ] (C) impedir o aninhamento de estruturas dentro de um documento.  
- [ ] (D) garantir integridade referencial declarativa entre coleções.  
- [ ] (E) armazenar exclusivamente dados numéricos.

---

**14**

O teorema CAP estabelece que um sistema distribuído de dados não é capaz de garantir simultaneamente as três propriedades

- [x] (A) consistência, disponibilidade e tolerância a particionamento.  
- [ ] (B) atomicidade, isolamento e durabilidade.  
- [ ] (C) confidencialidade, autenticidade e privacidade.  
- [ ] (D) completude, minimalidade e legibilidade.  
- [ ] (E) concorrência, atomicidade e persistência.

---

**15**

Em um sistema distribuído sujeito a partições de rede, uma equipe optou por manter o sistema respondendo a todas as requisições, ainda que alguns nós retornem dados desatualizados.

De acordo com o teorema CAP, essa escolha privilegia

- [ ] (A) consistência e tolerância a particionamento.  
- [x] (B) disponibilidade e tolerância a particionamento.  
- [ ] (C) consistência e disponibilidade.  
- [ ] (D) atomicidade e durabilidade.  
- [ ] (E) isolamento e consistência.

---

**16**

Diversos bancos de dados NoSQL adotam o modelo BASE, em contraposição ao modelo ACID dos bancos relacionais.

No modelo BASE, a consistência eventual significa que

- [ ] (A) o sistema nunca atinge um estado consistente entre seus nós.  
- [x] (B) todos os nós convergem para o mesmo estado após um intervalo de tempo, na ausência de novas atualizações.  
- [ ] (C) a consistência é verificada antes da confirmação de cada transação em todos os nós.  
- [ ] (D) as transações são serializadas em um único nó central.  
- [ ] (E) as restrições de integridade são verificadas exclusivamente na leitura.

---

**17**

Uma instituição financeira precisa registrar transferências bancárias, com garantia de que operações incompletas jamais sejam persistidas e de que as restrições de saldo sejam sempre respeitadas.

Para esse requisito, é mais adequado adotar

- [ ] (A) um banco de dados relacional com propriedades ACID.  
- [ ] (B) um banco de dados chave-valor com consistência eventual.  
- [ ] (C) um data lake com esquema definido na leitura.  
- [ ] (D) um banco de dados orientado a documentos sem esquema.  
- [ ] (E) um cubo OLAP multidimensional.

---

**18**

Um SGBD utiliza duas técnicas principais para controlar o acesso concorrente às mesmas informações.

A técnica que atribui bloqueios aos recursos acessados, impedindo que outra transação os utilize até a liberação, é o controle de concorrência

(A) pessimista, por bloqueio (locking).  
(B) otimista, por validação ao final da transação.  
(C) por versionamento multiversão sem bloqueio.  
(D) por particionamento horizontal dos dados.  
(E) por replicação assíncrona entre nós.

---

**19**

Os bancos de dados NoSQL apresentam características que os distinguem dos bancos relacionais.

**NÃO** constitui característica típica dos bancos de dados NoSQL a

(A) escalabilidade horizontal por meio da adição de nós.  
(B) flexibilidade de esquema entre registros de uma mesma coleção.  
(C) adoção frequente do modelo de consistência eventual.  
(D) garantia obrigatória de conformidade integral com as propriedades ACID.  
(E) adequação ao armazenamento de grandes volumes de dados heterogêneos.

---

**20**

Um analista relacionou funções desempenhadas por um Sistema Gerenciador de Banco de Dados.

**NÃO** constitui função de um SGBD a

(A) controle de acesso concorrente às informações armazenadas.  
(B) recuperação do banco de dados após falhas.  
(C) gerenciamento de autorizações e privilégios de usuários.  
(D) definição das regras de negócio da aplicação que consome os dados.  
(E) otimização das consultas submetidas ao banco.