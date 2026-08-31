---
Data: 2026-08-31
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**Considere as tabelas a seguir e suas instâncias para as questões 6, 7, 8, 9 e 10.**

**Funcionario**

|Matricula|Nome|ID_Depto|Salario|
|---|---|---|---|
|1|Ana|10|5000|
|2|Bruno|20|4000|
|3|Carla|10|6000|
|4|Diego|_(nulo)_|3000|
|5|Elisa|30|_(nulo)_|

**Departamento**

|ID_Depto|Nome|
|---|---|
|10|Vendas|
|20|TI|
|40|RH|

---

**1**

Os comandos da linguagem SQL são agrupados em sublinguagens conforme sua finalidade.

Os comandos `CREATE`, `ALTER` e `DROP` pertencem à

- [x] (A) Linguagem de Definição de Dados (DDL).  
- [ ] (B) Linguagem de Manipulação de Dados (DML).  
- [ ] (C) Linguagem de Controle de Dados (DCL).  
- [ ] (D) Linguagem de Controle de Transações (TCL).  
- [ ] (E) Linguagem de Consulta Estruturada exclusivamente.

---

**2**

Um administrador executou o comando a seguir.

sql

```sql
GRANT SELECT, INSERT ON Cliente TO analista_vendas;
```

Esse comando pertence à

- [ ] (A) Linguagem de Definição de Dados (DDL).  
- [x] (B) Linguagem de Manipulação de Dados (DML).  
- [ ] (C) Linguagem de Controle de Dados (DCL).  
- [ ] (D) Linguagem de Controle de Transações (TCL).  
- [ ] (E) Linguagem de consulta analítica multidimensional.

---

**3**

Uma equipe precisa remover todas as linhas de uma tabela com dez milhões de registros, preservando sua estrutura, com o menor custo de processamento e sem necessidade de registrar cada linha excluída individualmente no log.

O comando adequado a essa finalidade é

- [ ] (A) `DELETE FROM tabela;`  
- [x] (B) `TRUNCATE TABLE tabela;`  
- [ ] (C) `DROP TABLE tabela;`  
- [ ] (D) `ALTER TABLE tabela DROP COLUMN;`  
- [ ] (E) `UPDATE tabela SET coluna = NULL;`

---

**4**

Considere os comandos `DELETE`, `TRUNCATE` e `DROP`, aplicados a uma tabela existente.

Em relação a esses comandos, é correto afirmar que

- [ ] (A) os três removem a estrutura da tabela do banco de dados.  
- [x] (B) `DELETE` remove linhas e admite cláusula `WHERE`; `TRUNCATE` remove todas as linhas e preserva a estrutura; `DROP` remove a tabela e sua estrutura.  
- [ ] (C) `TRUNCATE` admite cláusula `WHERE` para remoção seletiva de linhas.  
- [ ] (D) `DROP` preserva a estrutura da tabela, removendo apenas seu conteúdo.  
- [ ] (E) `DELETE` pertence à DDL, enquanto `TRUNCATE` e `DROP` pertencem à DML.

---

**5**

Um analista precisa acrescentar uma restrição que garanta que a coluna `email` da tabela `Cliente`, já existente, não aceite valores duplicados.

O comando adequado é

- [x] (A) `ALTER TABLE Cliente ADD CONSTRAINT uk_email UNIQUE (email);`  
- [ ] (B) `UPDATE Cliente SET email = UNIQUE;`  
- [ ] (C) `CREATE UNIQUE Cliente (email);`  
- [ ] (D) `INSERT INTO Cliente CONSTRAINT UNIQUE (email);`  
- [ ] (E) `GRANT UNIQUE ON Cliente(email) TO PUBLIC;`

---

**6**

Considere o comando a seguir, executado sobre a tabela `Funcionario`.

sql

```sql
SELECT COUNT(*), COUNT(ID_Depto), COUNT(Salario)
FROM Funcionario;
```

O resultado retornado é, respectivamente,

- [ ] (A) 5, 5 e 5  
- [ ] (B) 5, 4 e 4  
- [x] (C) 4, 4 e 4  
- [ ] (D) 5, 5 e 4  
- [ ] (E) 3, 3 e 3

---

**7**

Considere o comando a seguir.

sql

```sql
SELECT AVG(Salario) FROM Funcionario;
```

O valor retornado é

- [ ] (A) 3600  
- [ ] (B) 4000  
- [x] (C) 4500  
- [ ] (D) 5000  
- [ ] (E) nulo, em razão da presença de valor nulo na coluna

---

**8**

Considere o comando a seguir.

sql

```sql
SELECT F.Nome, D.Nome
FROM   Funcionario F
INNER JOIN Departamento D ON F.ID_Depto = D.ID_Depto;
```

A quantidade de linhas retornadas por esse comando é

- [ ] (A) 2  
- [ ] (B) 3  
- [x] (C) 4  
- [ ] (D) 5  
- [ ] (E) 6

---

**9**

Um analista precisa listar os departamentos que não possuem nenhum funcionário associado.

O comando que atende a esse requisito é

- [ ] (A) `SELECT D.Nome FROM Departamento D INNER JOIN Funcionario F ON D.ID_Depto = F.ID_Depto WHERE F.Matricula IS NULL;`  
- [ ] (B) `SELECT D.Nome FROM Departamento D LEFT JOIN Funcionario F ON D.ID_Depto = F.ID_Depto WHERE F.Matricula IS NULL;`  
- [x] (C) `SELECT D.Nome FROM Departamento D LEFT JOIN Funcionario F ON D.ID_Depto = F.ID_Depto WHERE F.Matricula IS NOT NULL;`  
- [ ] (D) `SELECT D.Nome FROM Departamento D, Funcionario F WHERE D.ID_Depto = F.ID_Depto;`  
- [ ] (E) `SELECT D.Nome FROM Departamento D WHERE D.ID_Depto IS NULL;`

---

**10**

Considere o comando a seguir.

sql

```sql
SELECT ID_Depto, COUNT(*) AS Total
FROM   Funcionario
GROUP BY ID_Depto
HAVING COUNT(*) > 1;
```

O resultado retornado apresenta

- [ ] (A) nenhuma linha.  
- [ ] (B) uma linha, referente ao departamento 10.  
- [ ] (C) duas linhas, referentes aos departamentos 10 e 20.  
- [x] (D) três linhas, referentes aos departamentos 10, 20 e 30.  
- [ ] (E) quatro linhas, referentes a todos os departamentos e ao valor nulo.

---

**11**

As cláusulas `WHERE` e `HAVING` são utilizadas para filtrar dados em consultas SQL.

Uma diferença entre elas é que a cláusula `HAVING`

- [ ] (A) é aplicada antes do agrupamento, filtrando as linhas individuais.  
- [x] (B) é aplicada após o agrupamento, permitindo filtrar com base em funções de agregação.  
- [ ] (C) só pode ser utilizada em conjunto com a cláusula `ORDER BY`.  
- [ ] (D) substitui obrigatoriamente a cláusula `WHERE` em consultas com `GROUP BY`.  
- [ ] (E) pertence à Linguagem de Definição de Dados, enquanto `WHERE` pertence à DML.

---

**12**

Um analista executou os comandos a seguir.

sql

```sql
SELECT Cidade FROM Cliente
UNION
SELECT Cidade FROM Fornecedor;
```

Em relação ao resultado obtido, é correto afirmar que ele

- [x] (A) apresenta todas as ocorrências das duas consultas, inclusive as repetidas.  
- [ ] (B) elimina as linhas duplicadas entre as duas consultas.  
- [ ] (C) retorna apenas as cidades presentes simultaneamente nas duas tabelas.  
- [ ] (D) retorna apenas as cidades presentes na primeira tabela e ausentes na segunda.  
- [ ] (E) combina cada linha da primeira consulta com cada linha da segunda.

---

**13**

Um analista precisa executar uma consulta que retorne todas as linhas de duas consultas, incluindo as ocorrências repetidas, com o menor custo de processamento.

O operador adequado é

- [ ] (A) `UNION`  
- [x] (B) `UNION ALL`  
- [ ] (C) `INTERSECT`  
- [ ] (D) `EXCEPT`  
- [ ] (E) `CROSS JOIN`

---

**14**

Considere o comando a seguir, executado em um banco de dados de vendas.

sql

```sql
UPDATE Produto SET Preco = Preco * 1.10;
```

Em relação a esse comando, é correto afirmar que ele

- [ ] (A) será rejeitado, pois o comando `UPDATE` exige a cláusula `WHERE`.  
- [x] (B) atualizará o preço de todas as linhas da tabela Produto.  
- [ ] (C) atualizará apenas a primeira linha da tabela Produto.  
- [ ] (D) criará uma nova coluna com os preços atualizados.  
- [ ] (E) removerá as linhas cujo preço seja nulo.

---

**15**

Um analista precisa identificar os clientes que possuem ao menos um pedido registrado, utilizando subconsulta.

O comando que atende a esse requisito é

- [ ] (A) `SELECT Nome FROM Cliente C WHERE EXISTS (SELECT 1 FROM Pedido P WHERE P.ID_Cliente = C.ID_Cliente);`  
- [ ] (B) `SELECT Nome FROM Cliente C WHERE NOT EXISTS (SELECT 1 FROM Pedido P WHERE P.ID_Cliente = C.ID_Cliente);`  
- [ ] (C) `SELECT Nome FROM Cliente C WHERE C.ID_Cliente IS NOT NULL;`  
- [ ] (D) `SELECT Nome FROM Cliente C, Pedido P;`  
- [ ] (E) `SELECT Nome FROM Cliente C WHERE C.ID_Cliente NOT IN (SELECT ID_Cliente FROM Pedido);`

---

**16**

Considere a tabela `Empregado`, apresentada abaixo, que possui as colunas Empregado e Chefe.

|Empregado|Chefe|
|---|---|
|Ana|Bruno|
|Carla|Bruno|
|Bruno|Diego|
|Elisa|Carla|

Uma consulta SQL feita para exibir o nome do chefe do chefe de Ana retorna o nome Diego.

A expressão, em linguagem SQL, dessa consulta é

(A) `SELECT e2.chefe FROM Empregado e1 INNER JOIN Empregado e2 ON e1.chefe = e2.empregado WHERE e1.empregado = 'Ana';`

(B) `SELECT e1.chefe FROM Empregado e1 INNER JOIN Empregado e2 ON e1.chefe = e2.empregado WHERE e1.empregado = 'Ana';`

(C) `SELECT e2.chefe FROM Empregado e1 INNER JOIN Empregado e2 ON e1.empregado = e2.chefe WHERE e1.empregado = 'Ana';`

(D) `SELECT e2.empregado FROM Empregado e1 INNER JOIN Empregado e2 ON e1.chefe = e2.empregado WHERE e1.empregado = 'Ana';`

(E) `SELECT e2.chefe FROM Empregado e1 INNER JOIN Empregado e2 ON e1.chefe = e2.chefe WHERE e1.empregado = 'Ana';`

---

**17**

Um analista precisa criar um objeto que apresente, de forma permanente e consultável, o resultado de uma consulta que combina três tabelas, sem que os dados sejam fisicamente duplicados.

O comando adequado é

(A) `CREATE TABLE`  
(B) `CREATE VIEW`  
(C) `CREATE INDEX`  
(D) `INSERT INTO SELECT`  
(E) `CREATE SEQUENCE`

---

**18**

Considere o comando a seguir.

sql

```sql
SELECT Nome FROM Cliente
WHERE Cidade LIKE 'S%'
ORDER BY Nome DESC;
```

Esse comando retorna os nomes dos clientes

(A) cuja cidade termina com a letra S, ordenados de forma crescente.  
(B) cuja cidade começa com a letra S, ordenados de forma decrescente.  
(C) cuja cidade contém exatamente um caractere após a letra S.  
(D) de todas as cidades, ordenados pela coluna Cidade.  
(E) cuja cidade é igual ao literal 'S%', em ordem alfabética.

---

**19**

Os comandos SQL são classificados segundo sua sublinguagem.

**NÃO** é comando da Linguagem de Definição de Dados (DDL) o

(A) `CREATE`  
(B) `ALTER`  
(C) `DROP`  
(D) `UPDATE`  
(E) `TRUNCATE`

---

**20**

Um analista relacionou afirmações sobre comandos da linguagem SQL.

**NÃO** é característica dos comandos da Linguagem de Manipulação de Dados (DML) a

(A) inserção de novas linhas em tabelas existentes.  
(B) alteração de valores armazenados em colunas de tabelas.  
(C) remoção seletiva de linhas mediante condição.  
(D) modificação da estrutura das tabelas do banco de dados.  
(E) consulta aos dados armazenados nas tabelas.