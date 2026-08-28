---
Data: 2026-08-28
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Ao avaliar a qualidade de um modelo de dados, verifica-se se ele representa fielmente todos os requisitos levantados junto às áreas de negócio, sem omissões.

Esse critério de avaliação é denominado

- [x] (A) completude.  
- [ ] (B) minimalidade.  
- [ ] (C) legibilidade.  
- [ ] (D) desempenho.  
- [ ] (E) volatilidade.

---

**2**

Um modelo de dados é considerado **redundante** quando

- [x] (A) representa a mesma informação em mais de um ponto do modelo, sem necessidade.  
- [ ] (B) omite entidades identificadas durante o levantamento de requisitos.  
- [ ] (C) utiliza notação gráfica diferente da adotada pela organização.  
- [ ] (D) apresenta entidades sem atributos identificadores definidos.  
- [ ] (E) possui cardinalidades mínimas iguais a zero em todos os relacionamentos.

---

**3**

Durante a revisão de um modelo conceitual, identificou-se a entidade `Cliente` com o atributo `total_de_pedidos`, cujo valor pode ser obtido pela contagem dos pedidos associados a esse cliente.

Em relação a esse atributo, a avaliação correta é que ele

- [ ] (A) viola a Primeira Forma Normal, por não ser atômico.  
- [x] (B) constitui um atributo derivado, cuja manutenção no modelo deve ser justificada.  
- [ ] (C) caracteriza uma dependência multivalorada não trivial.  
- [ ] (D) impede a definição da chave primária da entidade Cliente.  
- [ ] (E) deve obrigatoriamente ser transformado em uma entidade fraca.

---

**4**

Considere o trecho de modelo conceitual a seguir, de um sistema hospitalar.

```
Paciente (1,n) —— Realiza —— (1,1) Consulta
Medico   (1,n) —— Atende  —— (1,1) Consulta
```

A área de negócio informou que um paciente pode agendar uma consulta sem que o médico tenha sido definido no momento do agendamento.

Diante dessa informação, o modelo apresenta

- [ ] (A) uma entidade fraca indevidamente representada.  
- [ ] (B) uma cardinalidade mínima incompatível com a regra de negócio informada.  
- [x] (C) um relacionamento ternário indevidamente decomposto.  
- [ ] (D) uma especialização total representada como parcial.  
- [ ] (E) uma agregação ausente entre Consulta e Medico.

---

**5**

Ao avaliar um modelo de dados, a equipe verifica se cada elemento representado é necessário, ou seja, se sua remoção provocaria perda de informação relevante.

Esse critério é denominado

- [x] (A) minimalidade.  
- [ ] (B) completude.  
- [ ] (C) integridade referencial.  
- [ ] (D) granularidade.  
- [ ] (E) volatilidade.

---

**6**

Considere o trecho de modelo lógico a seguir.

```
Empregado    (Matricula, Nome, ID_Cargo, Nome_Cargo)
Cargo        (ID_Cargo, Nome_Cargo, Salario_Base)
```

Na avaliação desse modelo, constata-se

- [ ] (A) ausência de chave primária na tabela Cargo.  
- [x] (B) redundância decorrente da repetição do atributo Nome_Cargo em duas relações.  
- [ ] (C) violação da integridade de entidade na tabela Empregado.  
- [ ] (D) impossibilidade de estabelecer relacionamento entre as duas relações.  
- [ ] (E) presença de atributo multivalorado na tabela Empregado.

---

**7**

Um analista revisou um modelo conceitual e constatou que a entidade `Endereco` possui apenas os atributos `logradouro`, `numero` e `cidade`, e participa de um único relacionamento (1,1) com a entidade `Cliente`, sem que exista requisito de reutilização de endereços.

Nesse caso, a avaliação mais adequada é que a entidade `Endereco`

- [ ] (A) deve ser transformada em entidade fraca de Cliente.  
- [x] (B) poderia ser representada como atributo composto de Cliente, simplificando o modelo.  
- [ ] (C) viola a Terceira Forma Normal por conter dependência transitiva.  
- [ ] (D) exige a criação de uma agregação com a entidade Cliente.  
- [ ] (E) deve ser especializada em subtipos por tipo de logradouro.

---

**8**

Considere o modelo lógico a seguir, de um sistema de biblioteca.

```
Livro     (ISBN, Titulo, Ano, ID_Editora)
Editora   (ID_Editora, Nome)
Emprestimo(ID_Emprestimo, Data, ISBN, Matricula_Usuario)
```

A área de negócio informou que um mesmo empréstimo pode conter vários livros.

Diante dessa informação, o modelo

- [ ] (A) atende ao requisito, pois a tabela Emprestimo já possui o atributo ISBN.  
- [ ] (B) não atende ao requisito, sendo necessária uma tabela associativa entre Emprestimo e Livro.  
- [ ] (C) não atende ao requisito, sendo necessário tornar ISBN um atributo multivalorado.  
- [ ] (D) atende ao requisito mediante a criação de um índice sobre a coluna ISBN.  
- [ ] (E) não atende ao requisito, sendo necessário eliminar a tabela Editora.

---

**9**

Ao avaliar modelos de dados, considera-se que um modelo possui boa **legibilidade** quando

(A) utiliza a menor quantidade possível de tabelas físicas.  
(B) é compreensível por seus leitores, com nomenclatura padronizada e organização clara.  
(C) dispensa a documentação de regras de negócio associadas.  
(D) apresenta desempenho superior nas consultas analíticas.  
(E) elimina completamente o uso de chaves substitutas.

---

**10**

Um modelo de dados foi construído com as entidades denominadas `TB01`, `TB02` e `TB03`, e com atributos nomeados `campo1`, `campo2` e `campo3`.

A principal deficiência desse modelo, do ponto de vista de avaliação de qualidade, é a

(A) ausência de integridade referencial entre as entidades.  
(B) baixa expressividade semântica da nomenclatura adotada.  
(C) violação da Segunda Forma Normal.  
(D) granularidade inadequada das tabelas de fato.  
(E) ausência de dimensões conformadas.

---

**11**

Durante a validação de um modelo conceitual junto às áreas de negócio, a equipe apresentou o diagrama entidade-relacionamento e percorreu, com os usuários, cada regra representada.

Essa prática tem por finalidade principal

(A) otimizar o desempenho das consultas que serão executadas.  
(B) confirmar se o modelo representa corretamente as regras do negócio.  
(C) definir os índices que serão criados no modelo físico.  
(D) estabelecer a política de backup do banco de dados.  
(E) determinar o particionamento físico das tabelas.

---

**12**

Considere o trecho de modelo conceitual a seguir.

```
Funcionario (0,n) —— Trabalha_em —— (0,n) Projeto
```

A área de negócio informou que todo projeto deve possuir, obrigatoriamente, ao menos um funcionário alocado.

A correção necessária no modelo consiste em alterar a cardinalidade

(A) mínima do lado Projeto para 1.  
(B) mínima do lado Funcionario para 1.  
(C) máxima do lado Projeto para 1.  
(D) máxima do lado Funcionario para 1.  
(E) mínima de ambos os lados para 1.

---

**13**

Um modelo de dados corporativo apresenta as entidades `Cliente`, `Comprador` e `Consumidor`, criadas por áreas diferentes, todas representando o mesmo conceito de negócio, com atributos praticamente idênticos.

Essa situação caracteriza um problema de

(A) granularidade.  
(B) integração e padronização semântica entre modelos.  
(C) integridade de entidade.  
(D) desnormalização excessiva.  
(E) dependência funcional transitiva.

---

**14**

Ao avaliar um modelo lógico, um analista constatou que determinada tabela possui quarenta e sete colunas, das quais trinta admitem valores nulos na maior parte das tuplas.

A hipótese mais provável a ser investigada nesse caso é a

(A) ausência de chave primária na tabela.  
(B) existência de subtipos distintos indevidamente representados em uma única tabela.  
(C) violação da integridade referencial com as demais tabelas.  
(D) necessidade de criação de índices sobre as colunas nulas.  
(E) presença de dimensões degeneradas no modelo.

---

**15**

Considere o modelo lógico a seguir, de um sistema acadêmico.

```
Aluno     (Matricula, Nome, Curso)
Professor (ID_Professor, Nome, Departamento)
Disciplina(ID_Disciplina, Nome, Carga_Horaria)
```

A área de negócio informou que é necessário registrar quais alunos cursam quais disciplinas e qual professor leciona cada disciplina.

Em relação a esses requisitos, o modelo apresenta

(A) completude adequada, pois todas as entidades necessárias estão representadas.  
(B) ausência de representação dos relacionamentos entre as entidades.  
(C) redundância entre as entidades Aluno e Professor.  
(D) violação da Primeira Forma Normal na entidade Disciplina.  
(E) granularidade inadequada na entidade Aluno.

---

**16**

Na avaliação de modelos de dados, a **flexibilidade** de um modelo refere-se à sua capacidade de

(A) executar consultas com o menor tempo de resposta possível.  
(B) acomodar mudanças futuras nos requisitos sem exigir reestruturação profunda.  
(C) armazenar o maior volume de dados no menor espaço físico.  
(D) dispensar a utilização de restrições de integridade.  
(E) ser convertido automaticamente em código-fonte de aplicação.

---

**17**

Um modelo de dados representa a entidade `Produto` com os atributos `preco_2024`, `preco_2025` e `preco_2026`.

Do ponto de vista da avaliação de qualidade, essa construção é inadequada porque

(A) viola a integridade de entidade da relação Produto.  
(B) exige alteração da estrutura da tabela a cada novo ano, comprometendo a flexibilidade.  
(C) impede a criação de chave estrangeira para a entidade Categoria.  
(D) caracteriza dependência funcional parcial em relação à chave primária.  
(E) torna obrigatória a adoção de um esquema em floco de neve.

---

**18**

Um analista compara duas propostas de modelo para o mesmo domínio de negócio. A primeira representa as regras corretamente, mas utiliza dezoito entidades. A segunda representa exatamente as mesmas regras, sem perda de informação, utilizando doze entidades.

Considerando-se os critérios de avaliação de modelos de dados, a segunda proposta é superior quanto à

(A) completude.  
(B) minimalidade.  
(C) integridade referencial.  
(D) aditividade das medidas.  
(E) volatilidade dos dados.

---

**19**

A avaliação de um modelo de dados considera diversos critérios de qualidade.

**NÃO** constitui critério de avaliação da qualidade de um modelo de dados a

(A) completude em relação aos requisitos levantados.  
(B) ausência de redundâncias desnecessárias.  
(C) clareza da nomenclatura utilizada.  
(D) quantidade de linhas de código da aplicação que acessará o banco.  
(E) correção das cardinalidades em relação às regras de negócio.

---

**20**

Um modelo de dados foi submetido a revisão técnica.

**NÃO** constitui indício de problema em um modelo de dados a

(A) presença de entidades sem qualquer relacionamento com as demais.  
(B) existência de atributos com o mesmo significado em múltiplas entidades.  
(C) utilização de chaves substitutas nas tabelas de dimensão de um data warehouse.  
(D) ausência de identificadores em determinadas entidades do modelo.  
(E) representação de um relacionamento N:M sem os atributos que lhe são próprios.