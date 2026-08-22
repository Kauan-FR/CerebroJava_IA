---
Data: 2026-08-22
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
**1**

Durante o projeto de um banco de dados, diz-se que existe uma dependência funcional entre os atributos X e Y de uma relação quando

- [ ] (A) X e Y pertencem ao mesmo domínio.  
- [x] (B) cada valor de X determina um único valor de Y.  
- [ ] (C) X e Y compõem, em conjunto, a chave primária da relação.  
- [ ] (D) X e Y podem assumir valores nulos simultaneamente.  
- [ ] (E) Y é obrigatoriamente uma chave estrangeira que referencia X.

---

**2**

Considere a tabela a seguir, utilizada por uma transportadora para registrar suas entregas.

|ID_Entrega|Destino|Itens_Transportados|
|---|---|---|
|501|Recife|Caixa A, Caixa B|
|502|Salvador|Caixa C|
|503|Natal|Caixa D, Caixa E, Caixa F|

Essa tabela não atende à Primeira Forma Normal (1FN) porque

- [ ] (A) não possui chave estrangeira definida.  
- [x] (B) apresenta um atributo cujos valores não são atômicos.  
- [ ] (C) possui chave primária composta por um único atributo.  
- [ ] (D) contém atributos que dependem transitivamente da chave primária.  
- [ ] (E) permite valores nulos na coluna Destino.

---

**3**

Uma relação encontra-se na Segunda Forma Normal (2FN) quando está na 1FN e

- [ ] (A) não possui atributos derivados.  
- [ ] (B) não possui dependências transitivas em relação à chave primária.  
- [x] (C) todo atributo não chave depende funcionalmente da totalidade da chave primária.  
- [ ] (D) todo determinante é uma superchave da relação.  
- [ ] (E) não possui atributos multivalorados nem grupos repetitivos.

---

**4**

Considere a relação a seguir, de um sistema de controle de vendas.

`ItemPedido (ID_Pedido, ID_Produto, Quantidade, Descricao_Produto, Preco_Unitario)`

A chave primária é composta por `ID_Pedido` e `ID_Produto`, e sabe-se que `Descricao_Produto` e `Preco_Unitario` dependem apenas de `ID_Produto`.

Essa relação viola a

- [ ] (A) Primeira Forma Normal, por conter atributos não atômicos.  
- [x] (B) Segunda Forma Normal, por conter dependência funcional parcial.  
- [ ] (C) Terceira Forma Normal, por conter dependência funcional transitiva.  
- [ ] (D) Forma Normal de Boyce-Codd, por possuir determinante que não é superchave.  
- [ ] (E) Quarta Forma Normal, por conter dependência multivalorada.

---

**5**

Considere a relação a seguir, de um sistema de recursos humanos.

`Empregado (Matricula, Nome, ID_Cargo, Nome_Cargo, Salario_Base_Cargo)`

A chave primária é `Matricula`, e sabe-se que `Nome_Cargo` e `Salario_Base_Cargo` são determinados por `ID_Cargo`.

Essa relação encontra-se

- [ ] (A) na 1FN, mas viola a 2FN.  
- [x] (B) na 2FN, mas viola a 3FN.  
- [ ] (C) na 3FN, mas viola a BCNF.  
- [ ] (D) na BCNF, sem qualquer violação.  
- [ ] (E) fora da 1FN, por possuir atributos redundantes.

---

**6**

Uma relação está na Terceira Forma Normal (3FN) quando está na 2FN e não apresenta

- [ ] (A) grupos repetitivos de atributos.  
- [ ] (B) dependência funcional parcial em relação à chave primária.  
- [ ] (C) dependência funcional transitiva entre atributos não chave e a chave primária.  
- [ ] (D) atributos que integrem mais de uma chave candidata.  
- [ ] (E) chaves estrangeiras que admitam valores nulos.

---

**7**

Uma tabela armazena, em conjunto, os dados dos cursos e os dados dos alunos matriculados. Ao excluir o último aluno matriculado em determinado curso, perdem-se também todas as informações sobre esse curso.

Essa situação caracteriza uma anomalia de

(A) inserção.  
(B) atualização.  
(C) exclusão.  
(D) concorrência.  
(E) integridade referencial.

---

**8**

Em uma tabela que armazena, simultaneamente, dados de empregados e de seus departamentos, não é possível cadastrar um novo departamento enquanto não houver ao menos um empregado lotado nele.

Essa limitação caracteriza uma anomalia de

(A) exclusão.  
(B) inserção.  
(C) atualização.  
(D) leitura não repetível.  
(E) violação de domínio.

---

**9**

A normalização de um banco de dados relacional tem por objetivo reduzir redundâncias e evitar anomalias.

Nesse contexto, **NÃO** constitui objetivo do processo de normalização

(A) eliminar dependências funcionais parciais.  
(B) reduzir a ocorrência de dados redundantes.  
(C) minimizar anomalias de inserção, atualização e exclusão.  
(D) aumentar a velocidade de leitura das consultas analíticas.  
(E) preservar a integridade semântica dos dados armazenados.

---

**10**

Ao decompor uma relação durante o processo de normalização, é fundamental garantir que a junção das relações resultantes reproduza exatamente o conteúdo original, sem gerar tuplas espúrias.

Essa propriedade é denominada decomposição

(A) sem perda de informação.  
(B) por dependência transitiva.  
(C) por projeção multivalorada.  
(D) irreversível.  
(E) horizontal.

---

**11**

Uma relação possui chave primária composta por um único atributo e todos os seus atributos são atômicos.

Em relação a essa relação, é correto afirmar que ela

(A) viola necessariamente a 2FN.  
(B) está automaticamente na 2FN, pois não há como existir dependência parcial.  
(C) está automaticamente na 3FN, pois não há como existir dependência transitiva.  
(D) está automaticamente na BCNF, pois possui chave simples.  
(E) não pode ser avaliada quanto às formas normais.

---

**12**

Considere a relação a seguir, de uma rede de lojas.

`Venda (ID_Venda, Data, ID_Vendedor, Nome_Vendedor, ID_Loja, Cidade_Loja)`

Sabe-se que `Nome_Vendedor` depende de `ID_Vendedor` e que `Cidade_Loja` depende de `ID_Loja`, sendo `ID_Venda` a chave primária.

A quantidade mínima de relações resultantes da normalização dessa tabela até a 3FN é

(A) 1  
(B) 2  
(C) 3  
(D) 4  
(E) 5

---

**13**

Considere a tabela a seguir, criada por uma clínica para registrar contatos de pacientes.

|ID_Paciente|Nome|Telefone_1|Telefone_2|Telefone_3|
|---|---|---|---|---|
|1|Ana|3021-1000|99988-1122|_(nulo)_|
|2|Bruno|3021-2000|_(nulo)_|_(nulo)_|

Essa estrutura caracteriza

(A) uma dependência transitiva entre Nome e Telefone.  
(B) um grupo repetitivo, que fere a Primeira Forma Normal.  
(C) uma dependência parcial em relação à chave primária.  
(D) uma violação da Forma Normal de Boyce-Codd.  
(E) uma decomposição com perda de informação.

---

**14**

Uma relação encontra-se na Forma Normal de Boyce-Codd (BCNF) quando, para toda dependência funcional não trivial X → Y presente na relação,

(A) Y é atributo não chave.  
(B) X é uma superchave da relação.  
(C) X e Y integram a mesma chave candidata.  
(D) Y depende parcialmente de X.  
(E) X não admite valores nulos.

---

**15**

Um analista afirma que determinada relação está na 3FN, porém não está na BCNF.

Essa situação pode ocorrer quando a relação possui

(A) atributos multivalorados na chave primária.  
(B) um determinante que não é superchave, envolvendo atributos de chaves candidatas sobrepostas.  
(C) chave primária composta por um único atributo.  
(D) dependência funcional parcial não eliminada.  
(E) atributos derivados calculados a partir da chave.

---

**16**

Após medir a lentidão dos relatórios gerenciais, uma equipe decidiu reintroduzir, de forma controlada, dados redundantes em determinadas tabelas do banco de dados.

Essa decisão de projeto físico é denominada

(A) normalização.  
(B) desnormalização.  
(C) decomposição sem perdas.  
(D) engenharia reversa.  
(E) particionamento vertical.

---

**17**

Considere a relação a seguir, de um sistema de gestão de projetos.

`Alocacao (ID_Empregado, ID_Projeto, Horas, Nome_Empregado)`

A chave primária é composta por `ID_Empregado` e `ID_Projeto`.

Nessa relação, o atributo `Nome_Empregado` estabelece uma dependência funcional

(A) total em relação à chave primária.  
(B) parcial em relação à chave primária.  
(C) transitiva em relação à chave primária.  
(D) multivalorada em relação à chave primária.  
(E) trivial em relação à chave primária.

---

**18**

As formas normais são progressivamente mais restritivas.

Nesse sentido, é correto afirmar que toda relação que se encontra na

(A) 2FN está necessariamente na 3FN.  
(B) 3FN está necessariamente na 2FN.  
(C) 1FN está necessariamente na 2FN.  
(D) 3FN está necessariamente na BCNF.  
(E) BCNF está necessariamente fora da 3FN.

---

**19**

Considere a tabela a seguir, de um sistema de controle de estoque.

|ID_Produto|Descricao|ID_Fornecedor|Nome_Fornecedor|Cidade_Fornecedor|
|---|---|---|---|---|
|10|Parafuso|500|Metalcorp|Recife|
|11|Porca|500|Metalcorp|Recife|
|12|Arruela|600|Ferrobras|Natal|

Caso o nome do fornecedor 500 seja alterado, será necessário atualizar mais de uma linha, sob risco de inconsistência.

Essa situação caracteriza uma anomalia de atualização decorrente de

(A) dependência funcional parcial.  
(B) dependência funcional transitiva.  
(C) dependência multivalorada.  
(D) ausência de chave estrangeira.  
(E) violação de integridade de entidade.

---

**20**

A Quarta Forma Normal (4FN) trata especificamente da eliminação de

(A) dependências funcionais parciais.  
(B) dependências funcionais transitivas.  
(C) dependências multivaloradas não triviais.  
(D) determinantes que não sejam superchaves.  
(E) atributos não atômicos.