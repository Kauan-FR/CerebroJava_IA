---
Data: 2026-08-20
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
**1**

No modelo relacional, cada linha de uma relação é formalmente denominada

- [ ] (A) atributo.  
- [ ] (B) domínio.  
- [x] (C) tupla.  
- [ ] (D) esquema.  
- [ ] (E) instância.

---

**2**

Considere a relação a seguir, que integra o banco de dados de uma distribuidora.

`Produto (ID_Produto, Descricao, Preco, ID_Categoria)`

O grau e a cardinalidade dessa relação correspondem, respectivamente, ao número de

- [ ] (A) tuplas e de atributos.  
- [x] (B) atributos e de tuplas.  
- [ ] (C) chaves candidatas e de tuplas.  
- [ ] (D) domínios e de restrições.  
- [ ] (E) atributos e de chaves estrangeiras.

---

**3**

Uma equipe discute os fundamentos do modelo relacional durante o projeto do banco de dados de um hospital.

Nesse modelo, o conjunto de valores permitidos para um determinado atributo é denominado

- [x] (A) domínio.  
- [ ] (B) esquema.  
- [ ] (C) grau.  
- [ ] (D) instância.  
- [ ] (E) chave candidata.

---

**4**

Considere o esquema relacional simplificado de um banco de dados de uma seguradora, contendo, ao menos, as seguintes tabelas:

```
Corretores (ID_Corretor, Nome, ID_Regional)
Apolices   (ID_Apolice, Valor, ID_Corretor)
```

Sabe-se que toda apólice é emitida por um corretor cadastrado.

A restrição que garante essa regra no modelo relacional é a integridade

- [ ] (A) de domínio.  
- [x] (B) de entidade.  
- [ ] (C) referencial.  
- [ ] (D) semântica.  
- [ ] (E) de unicidade.

---

**5**

Em uma tabela do modelo relacional, a restrição de integridade de entidade determina que

- [ ] (A) toda chave estrangeira referencie uma chave primária existente.  
- [x] (B) nenhum atributo da chave primária admita valor nulo.  
- [ ] (C) todo atributo pertença a um domínio previamente definido.  
- [ ] (D) toda relação possua ao menos uma chave estrangeira.  
- [ ] (E) nenhuma coluna da relação admita valores repetidos.

---

**6**

A tabela `Matricula` possui a chave estrangeira `ID_Curso`, que referencia a tabela `Curso`. Um analista precisa registrar matrículas de alunos que ainda não escolheram o curso.

Nessa situação, o modelo relacional

- [ ] (A) proíbe a operação, pois chaves estrangeiras não admitem valor nulo.  
- [x] (B) admite valor nulo na chave estrangeira, desde que ela não integre a chave primária.  
- [ ] (C) exige a criação de um curso fictício para manter a integridade referencial.  
- [ ] (D) converte automaticamente a chave estrangeira em chave alternativa.  
- [ ] (E) admite valor nulo apenas se a tabela Curso estiver vazia.

---

**7**

Considere as relações a seguir, de um sistema acadêmico.

```
Departamentos (ID_Departamento, Nome, Localizacao)
Professores   (ID_Professor, Nome, ID_Departamento)
```

Um analista tenta excluir o departamento de código 40, ao qual estão vinculados três professores, e a operação é rejeitada pelo SGBD.

O comportamento adotado pela chave estrangeira, nesse caso, é

- [ ] (A) CASCADE.  
- [ ] (B) SET NULL.  
- [ ] (C) SET DEFAULT.  
- [x] (D) RESTRICT.  
- [ ] (E) NO CHECK.

---

**8**

No modelo relacional, uma superchave distingue-se de uma chave candidata porque a superchave

- [x] (A) obrigatoriamente é composta por mais de um atributo.  
- [ ] (B) identifica unicamente as tuplas, mas pode conter atributos desnecessários.  
- [ ] (C) admite valores nulos em seus atributos componentes.  
- [ ] (D) só existe em relações que não possuem chave primária.  
- [ ] (E) é definida exclusivamente no modelo físico.

---

**9**

Considere a relação a seguir.

`Funcionario (Matricula, CPF, Nome, Email, ID_Setor)`

Sabe-se que `Matricula`, `CPF` e `Email` identificam unicamente cada funcionário, e que `Matricula` foi escolhida como chave primária.

Nesse caso, `CPF` e `Email` são classificados como chaves

- [ ] (A) estrangeiras.  
- [ ] (B) parciais.  
- [x] (C) alternativas.  
- [ ] (D) compostas.  
- [ ] (E) substitutas.

---

**10**

O esquema de uma relação, no modelo relacional, corresponde

- [x] (A) ao conjunto de tuplas armazenadas em determinado momento.  
- [ ] (B) à definição do nome da relação e de seus atributos com respectivos domínios.  
- [ ] (C) ao plano de execução gerado pelo otimizador de consultas.  
- [ ] (D) ao conjunto de índices criados sobre a relação.  
- [ ] (E) ao número de chaves estrangeiras que a relação possui.

---

**11**

Uma das características fundamentais do modelo relacional é que a ordem das tuplas em uma relação

- [x] (A) é irrelevante, pois a relação é definida como um conjunto.  
- [ ] (B) determina a eficiência da chave primária.  
- [ ] (C) deve corresponder à ordem de inserção dos registros.  
- [ ] (D) é definida obrigatoriamente pela chave estrangeira.  
- [ ] (E) segue sempre a ordem crescente da chave primária.

---

**12**

Considere a tabela a seguir, que registra os projetos de uma construtora.

|ID_Projeto|Nome|Responsaveis|
|---|---|---|
|1|Ponte Norte|Ana, Bruno|
|2|Viaduto Sul|Carla|

Essa tabela viola um princípio do modelo relacional porque

- [x] (A) não define chave estrangeira para os responsáveis.  
- [ ] (B) possui um atributo que armazena mais de um valor em uma mesma célula.  
- [ ] (C) apresenta tuplas duplicadas.  
- [ ] (D) não estabelece domínio para o atributo Nome.  
- [ ] (E) possui chave primária composta por um único atributo.

---

**13**

Um analista deve escolher, entre os operadores da Álgebra Relacional, aquele que retorna as tuplas presentes na primeira relação e ausentes na segunda.

Esse operador é a(o)

- [x] (A) união.  
- [ ] (B) interseção.  
- [ ] (C) diferença.  
- [ ] (D) divisão.  
- [ ] (E) produto cartesiano.

---

**14**

As relações `Cliente` e `Fornecedor` possuem, cada uma, os atributos `Nome` e `Cidade`, com domínios correspondentes. Um analista pretende obter uma única lista com todos os nomes e cidades registrados nas duas relações, sem repetições.

O operador da Álgebra Relacional adequado a essa finalidade é a(o)

- [ ] (A) junção natural.  
- [ ] (B) produto cartesiano.  
- [ ] (C) união.  
- [ ] (D) projeção.  
- [x] (E) divisão.

---

**15**

Considere as relações `Aluno`, com 40 tuplas e 5 atributos, e `Curso`, com 8 tuplas e 3 atributos.

O resultado do produto cartesiano entre essas duas relações possui

- [ ] (A) 48 tuplas e 8 atributos.  
- [ ] (B) 320 tuplas e 8 atributos.  
- [ ] (C) 320 tuplas e 15 atributos.  
- [x] (D) 48 tuplas e 15 atributos.  
- [ ] (E) 40 tuplas e 3 atributos.

---

**16**

Na Álgebra Relacional, a operação de junção natural entre duas relações distingue-se da equijunção porque a junção natural

- [ ] (A) admite condições que utilizem operadores diferentes da igualdade.  
- [x] (B) elimina, do resultado, a coluna duplicada correspondente ao atributo de junção.  
- [ ] (C) preserva as tuplas que não possuem correspondência na outra relação.  
- [ ] (D) não exige que as relações possuam atributos com o mesmo nome.  
- [ ] (E) é classificada como operador unário.

---

**17**

Considere as tabelas `Editora` e `Livro`, em que `Livro.ID_Editora` é chave estrangeira que referencia `Editora`. Existem editoras cadastradas que ainda não publicaram nenhum livro.

A consulta que retorna todas as editoras, inclusive aquelas sem livros associados, utiliza

- [ ] (A) junção interna.  
- [ ] (B) junção externa.  
- [ ] (C) produto cartesiano.  
- [x] (D) divisão.  
- [ ] (E) interseção.

---

**18**

Considere a tabela a seguir, de um sistema de controle acadêmico.

|ID_Aluno|ID_Disciplina|Nota|
|---|---|---|
|100|MAT01|8.5|
|100|FIS02|7.0|
|101|MAT01|9.0|

Sabe-se que um aluno pode cursar várias disciplinas e uma disciplina pode ser cursada por vários alunos.

A chave primária dessa tabela é

- [ ] (A) ID_Aluno.  
- [ ] (B) ID_Disciplina.  
- [ ] (C) a combinação de ID_Aluno e ID_Disciplina.  
- [ ] (D) a combinação de ID_Aluno, ID_Disciplina e Nota.  
- [ ] (E) uma chave substituta obrigatoriamente gerada pelo SGBD.

---

**19**

Um analista precisa identificar, na relação `Cursou (ID_Aluno, ID_Disciplina)`, os alunos que cursaram **todas** as disciplinas listadas na relação `Obrigatoria (ID_Disciplina)`.

O operador da Álgebra Relacional adequado a essa consulta é a(o)

(A) interseção.  
(B) divisão.  
(C) junção externa completa.  
(D) diferença.  
(E) seleção.

---

**20**

Considere a relação `Empregado`, apresentada abaixo, que possui as colunas Gerente e Subordinado.

|Gerente|Subordinado|
|---|---|
|Alberto|Bianca|
|Alberto|Caio|
|Bianca|Denise|
|Bianca|Eduardo|
|Caio|Flavia|
|Denise|Gabriel|

Uma consulta SQL feita para exibir os nomes dos subordinados dos subordinados de Alberto retorna os nomes Denise, Eduardo e Flavia.

A expressão, em linguagem SQL, dessa consulta é

(A) `SELECT e2.subordinado FROM Empregado e1 INNER JOIN Empregado e2 ON e1.subordinado = e2.gerente WHERE e1.gerente = 'Alberto';`

(B) `SELECT e1.gerente FROM Empregado e1 INNER JOIN Empregado e2 ON e1.gerente = e2.subordinado WHERE e1.subordinado = 'Alberto';`

(C) `SELECT e2.subordinado FROM Empregado e1 INNER JOIN Empregado e2 ON e1.gerente = e2.gerente WHERE e1.gerente = 'Alberto';`

(D) `SELECT e1.subordinado FROM Empregado e1 INNER JOIN Empregado e2 ON e1.subordinado = e2.gerente WHERE e1.gerente = 'Alberto';`

(E) `SELECT e2.subordinado FROM Empregado e1 INNER JOIN Empregado e2 ON e1.subordinado = e2.subordinado WHERE e1.gerente = 'Alberto';`