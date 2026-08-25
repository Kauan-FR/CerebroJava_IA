---
Data: 2026-08-25
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

No modelo relacional, a restrição de integridade referencial estabelece que

- [ ] (A) nenhum atributo da chave primária pode assumir valor nulo.  
- [x] (B) todo valor de uma chave estrangeira deve corresponder a um valor existente na chave referenciada ou ser nulo.  
- [ ] (C) todo atributo deve assumir valores pertencentes a um domínio previamente definido.  
- [ ] (D) toda relação deve possuir ao menos uma chave estrangeira declarada.  
- [ ] (E) nenhuma coluna de uma relação pode conter valores duplicados.

---

**2**

Considere a relação a seguir, de um sistema de controle patrimonial.

`Bem (ID_Bem, Descricao, ID_Setor)`

Uma tentativa de inserir uma tupla com `ID_Bem` nulo é rejeitada pelo SGBD.

A restrição violada nessa operação é a integridade

- [ ] (A) referencial.  
- [ ] (B) de domínio.  
- [x] (C) de entidade.  
- [ ] (D) semântica.  
- [ ] (E) de unicidade.

---

**3**

A coluna `situacao` da tabela `Contrato` foi definida para aceitar exclusivamente os valores 'ATIVO', 'SUSPENSO' e 'ENCERRADO'. Uma tentativa de gravar o valor 'CANCELADO' é rejeitada.

A restrição violada nessa operação é a integridade

- [ ] (A) de entidade.  
- [ ] (B) referencial.  
- [x] (C) de domínio.  
- [ ] (D) de chave estrangeira.  
- [ ] (E) de decomposição.

---

**4**

Considere as tabelas a seguir, de um sistema acadêmico.

```
Orientadores (ID_Orientador, Nome)
Alunos       (ID_Aluno, Nome, ID_Orientador)
```

Sabe-se que nem todo aluno possui orientador designado.

Em relação à coluna `ID_Orientador` da tabela `Alunos`, é correto afirmar que ela

- [ ] (A) não pode ser declarada como chave estrangeira, pois admite valores nulos.  
- [x] (B) pode ser declarada como chave estrangeira e admitir valores nulos, desde que não integre a chave primária.  
- [ ] (C) deve ser preenchida obrigatoriamente com um valor padrão para preservar a integridade referencial.  
- [ ] (D) deve ser convertida em chave alternativa da tabela Alunos.  
- [ ] (E) exige a criação de uma tupla fictícia na tabela Orientadores.

---

**5**

Considere a definição a seguir, de um sistema de vendas.

sql

```sql
CREATE TABLE ItemPedido (
  ID_Pedido  INT,
  ID_Produto INT,
  Quantidade INT,
  PRIMARY KEY (ID_Pedido, ID_Produto),
  FOREIGN KEY (ID_Pedido) REFERENCES Pedido(ID_Pedido)
    ON DELETE SET NULL
);
```

Uma inconsistência nessa definição é que a cláusula `ON DELETE SET NULL`

(A) não pode ser aplicada a chaves estrangeiras compostas.  
(B) tentaria atribuir valor nulo a uma coluna que integra a chave primária.  
(C) exige a declaração prévia de um valor padrão para a coluna.  
(D) só é válida em conjunto com a cláusula ON UPDATE RESTRICT.  
(E) impede a criação de índices sobre a tabela ItemPedido.

---

**6**

Em um sistema de recursos humanos, a chave estrangeira `ID_Departamento` da tabela `Empregado` foi declarada com a cláusula `ON DELETE SET NULL`.

Ao se excluir um departamento que possui empregados vinculados,

(A) a exclusão é rejeitada pelo SGBD.  
(B) os empregados vinculados são também excluídos.  
(C) a coluna ID_Departamento dos empregados vinculados passa a conter valor nulo.  
(D) a coluna ID_Departamento dos empregados vinculados recebe o valor padrão definido.  
(E) os empregados vinculados são transferidos para o departamento de menor código.

---

**7**

Considere as tabelas `Pedido` e `ItemPedido`, em que a chave estrangeira de `ItemPedido` referencia `Pedido` com a cláusula `ON DELETE CASCADE`.

Ao se executar a exclusão de um pedido que possui cinco itens associados, ocorrerá

(A) a rejeição da operação, em razão da dependência existente.  
(B) a exclusão do pedido e dos cinco itens associados.  
(C) a exclusão do pedido, permanecendo os cinco itens com chave estrangeira nula.  
(D) a exclusão apenas dos cinco itens, permanecendo o pedido.  
(E) a exclusão do pedido, permanecendo os cinco itens com chave estrangeira inalterada.

---

**8**

O código de um curso, definido como chave primária da tabela `Curso`, foi alterado de 'ADS' para 'ADS2'. A tabela `Matricula` possui chave estrangeira que referencia `Curso` e está declarada com a cláusula `ON UPDATE CASCADE`.

Nessa situação, as tuplas de `Matricula` que referenciavam o curso 'ADS'

(A) passam a referenciar o valor 'ADS2' automaticamente.  
(B) são excluídas automaticamente pelo SGBD.  
(C) passam a conter valor nulo na chave estrangeira.  
(D) permanecem inalteradas, gerando tuplas órfãs.  
(E) impedem a alteração da chave primária da tabela Curso.

---

**9**

Considere o esquema relacional simplificado do banco de dados de uma seguradora, contendo, ao menos, as seguintes tabelas:

```
Regionais  (ID_Regional, Nome, UF)
Corretores (ID_Corretor, Nome, ID_Regional)
Apolices   (ID_Apolice, Valor, ID_Corretor)
```

Entre outras restrições que devem ser consideradas, sabe-se que todo corretor pertence a uma regional e que toda apólice é emitida por um corretor cadastrado.

Considerando-se o esquema apresentado, o trecho de código em linguagem SQL DDL que respeita todas as restrições de integridade citadas é

(A)

sql

```sql
CREATE TABLE Regionais (
  ID_Regional INT PRIMARY KEY,
  Nome VARCHAR(100),
  UF CHAR(2)
);
CREATE TABLE Corretores (
  ID_Corretor INT PRIMARY KEY,
  Nome VARCHAR(100),
  ID_Regional INT
);
CREATE TABLE Apolices (
  ID_Apolice INT PRIMARY KEY,
  Valor DECIMAL(10,2),
  ID_Corretor INT
);
```

(B)

sql

```sql
CREATE TABLE Regionais (
  ID_Regional INT PRIMARY KEY,
  Nome VARCHAR(100),
  UF CHAR(2)
);
CREATE TABLE Corretores (
  ID_Corretor INT PRIMARY KEY,
  Nome VARCHAR(100),
  ID_Regional INT,
  FOREIGN KEY (ID_Regional) REFERENCES Regionais(ID_Regional)
);
CREATE TABLE Apolices (
  ID_Apolice INT PRIMARY KEY,
  Valor DECIMAL(10,2),
  ID_Corretor INT
);
```

(C)

sql

```sql
CREATE TABLE Regionais (
  ID_Regional INT PRIMARY KEY,
  Nome VARCHAR(100),
  UF CHAR(2)
);
CREATE TABLE Corretores (
  ID_Corretor INT PRIMARY KEY,
  Nome VARCHAR(100),
  ID_Regional INT,
  FOREIGN KEY (ID_Regional) REFERENCES Regionais(ID_Regional)
);
CREATE TABLE Apolices (
  ID_Apolice INT PRIMARY KEY,
  Valor DECIMAL(10,2),
  ID_Corretor INT,
  FOREIGN KEY (ID_Corretor) REFERENCES Corretores(ID_Corretor)
);
```

(D)

sql

```sql
CREATE TABLE Regionais (
  ID_Regional INT PRIMARY KEY,
  Nome VARCHAR(100),
  UF CHAR(2)
);
CREATE TABLE Corretores (
  ID_Corretor INT PRIMARY KEY,
  Nome VARCHAR(100),
  ID_Regional INT,
  FOREIGN KEY (ID_Regional) REFERENCES Apolices(ID_Apolice)
);
CREATE TABLE Apolices (
  ID_Apolice INT PRIMARY KEY,
  Valor DECIMAL(10,2),
  ID_Corretor INT,
  FOREIGN KEY (ID_Corretor) REFERENCES Corretores(ID_Corretor)
);
```

(E)

sql

```sql
CREATE TABLE Regionais (
  ID_Regional INT,
  Nome VARCHAR(100),
  UF CHAR(2)
);
CREATE TABLE Corretores (
  ID_Corretor INT,
  Nome VARCHAR(100),
  ID_Regional INT,
  FOREIGN KEY (ID_Regional) REFERENCES Regionais(ID_Regional)
);
CREATE TABLE Apolices (
  ID_Apolice INT,
  Valor DECIMAL(10,2),
  ID_Corretor INT,
  FOREIGN KEY (ID_Corretor) REFERENCES Corretores(ID_Corretor)
);
```

---

**10**

Considere as tabelas a seguir e suas instâncias.

**Departamento**

|ID_Departamento|Nome|
|---|---|
|10|Vendas|
|20|TI|

**Empregado**

|Matricula|Nome|ID_Departamento|
|---|---|---|
|1|Ana|10|
|2|Bruno|20|

Sabe-se que `Empregado.ID_Departamento` é chave estrangeira que referencia `Departamento`.

O comando que será rejeitado pelo SGBD, por violação de integridade referencial, é

(A) `INSERT INTO Empregado VALUES (3, 'Carla', 10);`  
(B) `INSERT INTO Empregado VALUES (4, 'Diego', 30);`  
(C) `INSERT INTO Departamento VALUES (30, 'Juridico');`  
(D) `UPDATE Empregado SET ID_Departamento = 20 WHERE Matricula = 1;`  
(E) `DELETE FROM Empregado WHERE Matricula = 2;`

---

**11**

Uma equipe precisa carregar dados em duas tabelas relacionadas por chave estrangeira, sem que as restrições de integridade sejam violadas durante a carga.

A ordem correta de inserção é

(A) primeiro na tabela que contém a chave estrangeira, depois na tabela referenciada.  
(B) primeiro na tabela referenciada, depois na tabela que contém a chave estrangeira.  
(C) indiferente, pois a integridade referencial só é verificada ao final da transação.  
(D) simultânea, exigindo obrigatoriamente o uso de gatilhos.  
(E) determinada pela ordem alfabética dos nomes das tabelas.

---

**12**

Considere a tabela a seguir, de um sistema de gestão de pessoas.

`Empregado (Matricula, Nome, Matricula_Supervisor)`

Sabe-se que todo empregado, exceto o presidente da empresa, é supervisionado por outro empregado.

Nesse caso, a coluna `Matricula_Supervisor` é

(A) uma chave estrangeira que referencia a própria tabela Empregado.  
(B) uma chave alternativa da tabela Empregado.  
(C) um atributo multivalorado da tabela Empregado.  
(D) parte obrigatória da chave primária da tabela Empregado.  
(E) incompatível com o modelo relacional, por gerar referência circular.

---

**13**

Em uma tabela `Funcionario`, a coluna `matricula` foi definida como chave primária e a coluna `cpf`, com restrição UNIQUE. Um analista pretende criar, em outra tabela, uma chave estrangeira que referencie o CPF do funcionário.

Nessa situação, a chave estrangeira

(A) não pode ser criada, pois só é possível referenciar chaves primárias.  
(B) pode ser criada, pois é possível referenciar colunas com restrição UNIQUE.  
(C) só pode ser criada se a restrição UNIQUE for convertida em chave primária.  
(D) só pode ser criada se a coluna cpf não admitir valores nulos.  
(E) exige a remoção da chave primária matricula.

---

**14**

Considere as tabelas a seguir.

```
Turma      (ID_Curso, ID_Periodo, Sala)
Frequencia (ID_Aluno, ID_Curso, ID_Periodo, Faltas)
```

A chave primária de `Turma` é composta por `ID_Curso` e `ID_Periodo`.

Para garantir a integridade referencial entre `Frequencia` e `Turma`, deve-se declarar

(A) duas chaves estrangeiras independentes, uma para ID_Curso e outra para ID_Periodo.  
(B) uma única chave estrangeira composta pelas colunas ID_Curso e ID_Periodo.  
(C) uma chave estrangeira apenas para ID_Curso, por ser o primeiro atributo da chave.  
(D) uma chave estrangeira que referencie a coluna Sala da tabela Turma.  
(E) uma chave alternativa em Frequencia, dispensando a chave estrangeira.

---

**15**

Considere as tabelas `Categoria` e `Produto`, em que `Produto.ID_Categoria` é chave estrangeira que referencia `Categoria.ID_Categoria`. A tabela `Categoria` possui tuplas referenciadas por produtos cadastrados.

A execução do comando `DROP TABLE Categoria` resultará em

(A) sucesso, com exclusão automática da tabela Produto.  
(B) sucesso, com atribuição de valor nulo à coluna ID_Categoria.  
(C) erro, em razão da dependência existente, salvo se a remoção for executada em cascata.  
(D) erro, pois tabelas referenciadas não podem ser removidas em hipótese alguma.  
(E) sucesso, com conversão automática da chave estrangeira em coluna comum.

---

**16**

Um analista removeu, de um banco de dados em produção, todas as cláusulas FOREIGN KEY, mantendo as colunas correspondentes nas tabelas.

Uma consequência esperada dessa alteração é

(A) a impossibilidade de executar operações de junção entre as tabelas.  
(B) o surgimento de tuplas órfãs, com referências a valores inexistentes.  
(C) a perda imediata dos dados das colunas envolvidas.  
(D) a conversão automática das chaves primárias em chaves candidatas.  
(E) a violação da restrição de integridade de entidade.

---

**17**

Uma instituição financeira exige que o valor da coluna `data_encerramento` de uma conta seja sempre posterior ao valor da coluna `data_abertura`.

Essa regra caracteriza uma restrição de integridade

(A) de entidade, implementada por PRIMARY KEY.  
(B) referencial, implementada por FOREIGN KEY.  
(C) semântica, definida pelo usuário e implementada por CHECK.  
(D) de domínio, implementada pela escolha do tipo de dado.  
(E) de unicidade, implementada por UNIQUE.

---

**18**

A declaração de uma chave estrangeira produz diversos efeitos sobre o comportamento do banco de dados.

**NÃO** constitui efeito da declaração de uma chave estrangeira a

(A) rejeição de inserções que referenciem valores inexistentes na tabela referenciada.  
(B) restrição às operações de exclusão na tabela referenciada, conforme a ação declarada.  
(C) garantia de que a coluna referenciadora não conterá valores duplicados.  
(D) possibilidade de propagação automática de alterações, conforme a ação declarada.  
(E) criação de dependência entre as tabelas envolvidas.

---

**19**

Considere as tabelas a seguir e suas instâncias.

**Cliente**

|ID_Cliente|Nome|
|---|---|
|1|Ana|
|2|Bruno|

**Pedido**

|ID_Pedido|ID_Cliente|
|---|---|
|100|1|
|101|1|
|102|2|

**ItemPedido**

|ID_Item|ID_Pedido|
|---|---|
|900|100|
|901|101|
|902|102|

As chaves estrangeiras `Pedido.ID_Cliente` e `ItemPedido.ID_Pedido` foram ambas declaradas com `ON DELETE CASCADE`.

Após a execução de `DELETE FROM Cliente WHERE ID_Cliente = 1`, a quantidade de tuplas restantes nas tabelas `Pedido` e `ItemPedido` será, respectivamente,

(A) 3 e 3  
(B) 2 e 2  
(C) 1 e 1  
(D) 1 e 3  
(E) 0 e 0

---

**20**

Um analista precisa diferenciar as restrições de integridade aplicáveis a um banco de dados relacional.

Nesse contexto, as integridades de entidade e referencial incidem, respectivamente, sobre

(A) a chave estrangeira e a chave primária.  
(B) a chave primária e a chave estrangeira.  
(C) o domínio dos atributos e a chave primária.  
(D) a chave primária e o domínio dos atributos.  
(E) as chaves candidatas e as chaves alternativas.