---
Data: 2026-08-31
---
---

**Considere as tabelas a seguir e suas instâncias para as questões 1 a 8.**

**Cliente**

|ID_Cliente|Nome|Cidade|Limite|
|---|---|---|---|
|1|Ana|Recife|5000|
|2|Bruno|Salvador|_(nulo)_|
|3|Carla|Recife|8000|
|4|Diego|Natal|3000|
|5|Elisa|_(nulo)_|3000|

**Pedido**

|ID_Pedido|ID_Cliente|Valor|Status|
|---|---|---|---|
|100|1|1200|ENTREGUE|
|101|1|800|PENDENTE|
|102|3|2500|ENTREGUE|
|103|3|1500|CANCELADO|
|104|6|900|ENTREGUE|
|105|_(nulo)_|400|PENDENTE|

---

**1**

sql

```sql
SELECT COUNT(*), COUNT(Cidade), COUNT(DISTINCT Cidade)
FROM Cliente;
```

O resultado retornado é, respectivamente,

- [ ] (A) 5, 5 e 4  
- [x] (B) 5, 4 e 3  
- [ ] (C) 4, 4 e 3  
- [ ] (D) 5, 4 e 4  
- [ ] (E) 5, 5 e 3

---

**2**

sql

```sql
SELECT SUM(Limite), AVG(Limite), MAX(Limite)
FROM Cliente;
```

O resultado retornado é, respectivamente,

- [ ] (A) 19000, 3800 e 8000  
- [x] (B) 19000, 4750 e 8000  
- [ ] (C) 19000, 4750 e nulo  
- [ ] (D) nulo, nulo e nulo  
- [ ] (E) 24000, 4800 e 8000

---

**3**

sql

```sql
SELECT C.Nome, P.Valor
FROM   Cliente C
INNER JOIN Pedido P ON C.ID_Cliente = P.ID_Cliente;
```

A quantidade de linhas retornadas é

- [ ] (A) 3  
- [x] (B) 4  
- [ ] (C) 5  
- [ ] (D) 6  
- [ ] (E) 7

---

**4**

sql

```sql
SELECT C.Nome, P.Valor
FROM   Cliente C
LEFT JOIN Pedido P ON C.ID_Cliente = P.ID_Cliente;
```

A quantidade de linhas retornadas é

- [ ] (A) 4  
- [x] (B) 5  
- [ ] (C) 6  
- [ ] (D) 7  
- [ ] (E) 8

---

**5**

sql

```sql
SELECT C.Nome
FROM   Cliente C
LEFT JOIN Pedido P ON C.ID_Cliente = P.ID_Cliente
WHERE  P.ID_Pedido IS NULL;
```

O resultado retornado apresenta os nomes

- [ ] (A) Ana e Carla.  
- [x] (B) Bruno, Diego e Elisa.  
- [ ] (C) Ana, Bruno, Carla, Diego e Elisa.  
- [ ] (D) apenas Elisa.  
- [ ] (E) nenhuma linha.

---

**6**

sql

```sql
SELECT ID_Cliente, COUNT(*) AS Qtd, SUM(Valor) AS Total
FROM   Pedido
GROUP BY ID_Cliente
HAVING SUM(Valor) > 2000;
```

O resultado retornado apresenta

- [ ] (A) nenhuma linha.  
- [x] (B) uma linha, referente ao cliente 3.  
- [ ] (C) duas linhas, referentes aos clientes 1 e 3.  
- [ ] (D) três linhas, referentes aos clientes 1, 3 e 6.  
- [ ] (E) quatro linhas, incluindo a do valor nulo.

---

**7**

sql

```sql
SELECT ID_Cliente, COUNT(*) AS Qtd
FROM   Pedido
WHERE  Status = 'ENTREGUE'
GROUP BY ID_Cliente;
```

O resultado retornado apresenta

- [ ] (A) uma linha: cliente 1 com 2.  
- [ ] (B) duas linhas: cliente 1 com 1 e cliente 3 com 1.  
- [x] (C) três linhas: cliente 1 com 1, cliente 3 com 1 e cliente 6 com 1.  
- [ ] (D) três linhas: cliente 1 com 2, cliente 3 com 2 e cliente 6 com 1.  
- [ ] (E) quatro linhas, incluindo a do cliente nulo.

---

**8**

sql

```sql
SELECT Nome FROM Cliente
WHERE  ID_Cliente NOT IN (SELECT ID_Cliente FROM Pedido);
```

O resultado retornado apresenta

- [x] (A) Bruno, Diego e Elisa.  
- [ ] (B) Ana e Carla.  
- [ ] (C) todos os cinco clientes.  
- [ ] (D) nenhuma linha.  
- [ ] (E) apenas Diego.

---

**Considere as tabelas a seguir e suas instâncias para as questões 9 a 12.**

**Produto**

|ID_Produto|Descricao|ID_Categoria|Preco|
|---|---|---|---|
|10|Parafuso|1|2|
|11|Porca|1|3|
|12|Arruela|2|1|
|13|Prego|_(nulo)_|5|

**Categoria**

|ID_Categoria|Nome|
|---|---|
|1|Fixação|
|2|Acessórios|
|3|Ferramentas|

---

**9**

sql

```sql
SELECT COUNT(*)
FROM   Produto P
RIGHT JOIN Categoria C ON P.ID_Categoria = C.ID_Categoria;
```

O resultado retornado é

- [x] (A) 2  
- [ ] (B) 3  
- [ ] (C) 4  
- [ ] (D) 5  
- [ ] (E) 6

---

**10**

sql

```sql
SELECT C.Nome, COUNT(P.ID_Produto) AS Qtd
FROM   Categoria C
LEFT JOIN Produto P ON C.ID_Categoria = P.ID_Categoria
GROUP BY C.Nome;
```

O resultado retornado apresenta

- [ ] (A) Fixação com 2, Acessórios com 1 e Ferramentas com 0.  
- [ ] (B) Fixação com 2, Acessórios com 1 e Ferramentas com 1.  
- [ ] (C) Fixação com 2 e Acessórios com 1, apenas.  
- [ ] (D) Fixação com 2, Acessórios com 1, Ferramentas com 0 e uma linha nula com 1.  
- [ ] (E) todas as categorias com 1.

---

**11**

sql

```sql
SELECT COUNT(*)
FROM   Produto, Categoria;
```

O resultado retornado é

(A) 4  
(B) 7  
(C) 9  
(D) 12  
(E) 16

---

**12**

sql

```sql
SELECT Descricao FROM Produto
WHERE  Preco > (SELECT AVG(Preco) FROM Produto);
```

O resultado retornado apresenta

(A) Parafuso e Porca.  
(B) Prego, apenas.  
(C) Porca e Prego.  
(D) Arruela, apenas.  
(E) nenhuma linha.

---

**Considere a tabela a seguir e sua instância para as questões 13 a 15.**

**Cargo**

|Funcionario|Superior|
|---|---|
|Ana|Bruno|
|Bruno|Carla|
|Carla|Diego|
|Elisa|Bruno|
|Fabio|Ana|

---

**13**

Uma consulta SQL feita para exibir o nome do superior do superior de Ana retorna o nome Carla.

A expressão, em linguagem SQL, dessa consulta é

(A) `SELECT c2.superior FROM Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.funcionario WHERE c1.funcionario = 'Ana';`

(B) `SELECT c1.superior FROM Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.funcionario WHERE c1.funcionario = 'Ana';`

(C) `SELECT c2.superior FROM Cargo c1 INNER JOIN Cargo c2 ON c1.funcionario = c2.superior WHERE c1.funcionario = 'Ana';`

(D) `SELECT c2.funcionario FROM Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.funcionario WHERE c1.funcionario = 'Ana';`

(E) `SELECT c2.superior FROM Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.superior WHERE c1.funcionario = 'Ana';`

---

**14**

sql

```sql
SELECT c1.funcionario
FROM   Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.funcionario
WHERE  c2.superior = 'Carla';
```

O resultado retornado apresenta

(A) Ana e Elisa.  
(B) Bruno, apenas.  
(C) Ana, apenas.  
(D) Carla e Diego.  
(E) nenhuma linha.

---

**15**

sql

```sql
SELECT COUNT(*)
FROM   Cargo c1 INNER JOIN Cargo c2 ON c1.superior = c2.funcionario;
```

O resultado retornado é

(A) 3  
(B) 4  
(C) 5  
(D) 6  
(E) 25