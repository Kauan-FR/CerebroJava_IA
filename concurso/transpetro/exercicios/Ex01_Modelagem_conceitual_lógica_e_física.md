---
Data: 2026-08-13
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
**1**

Uma seguradora iniciou o projeto do banco de dados de seu novo sistema de apólices, organizando o trabalho em níveis de abstração distintos.

O modelo conceitual caracteriza-se por

- [ ] (A) especificar índices, partições e estruturas de armazenamento das tabelas.  
- [x] (B) representar os requisitos de dados do negócio independentemente do SGBD a ser adotado.  
- [ ] (C) definir tipos de dados e restrições em conformidade com o SGBD escolhido.  
- [ ] (D) descrever tabelas, colunas e chaves estrangeiras já ajustadas ao produto contratado.  
- [ ] (E) ser obtido automaticamente a partir do modelo físico por meio de engenharia reversa.

---

**2**

Uma rede hoteleira modelou as entidades Hóspede e Dependente. Um dependente só existe vinculado a um hóspede, e seu nome se repete entre hóspedes diferentes.

A entidade Dependente é classificada como entidade fraca porque

- [ ] (A) possui uma quantidade reduzida de atributos.  
- [ ] (B) não possui atributos próprios além do relacionamento.  
- [x] (C) depende de outra entidade para ter sua identificação completa.  
- [ ] (D) participa do relacionamento com cardinalidade máxima igual a 1.  
- [ ] (E) só passa a existir a partir do modelo lógico.

---

**3**

No modelo conceitual de um sistema de recursos humanos, a entidade Empregado possui o atributo data_nascimento. A área de negócio solicitou que a idade do empregado também estivesse disponível nas consultas.

No modelo conceitual, a idade deve ser representada como atributo

- [ ] (A) composto.  
- [ ] (B) multivalorado.  
- [ ] (C) derivado.  
- [ ] (D) identificador.  
- [ ] (E) discriminador.

---

**4**

Na modelagem de um sistema comercial, definiu-se que um cliente pode cadastrar diversos números de telefone e que seu endereço é formado por logradouro, número, bairro e cidade.

Os atributos telefone e endereço são classificados, respectivamente, como

(A) multivalorado e composto.  
(B) composto e multivalorado.  
(C) derivado e composto.  
(D) multivalorado e derivado.  
(E) composto e opcional.

---

**5**

O diagrama E-R a seguir representa parte do modelo conceitual de uma clínica.

`Médico (1,n) —— Realiza —— (1,1) Consulta`

Infere-se, pela leitura desse modelo, que

(A) um médico realiza, no máximo, uma consulta.  
(B) toda consulta é realizada por exatamente um médico.  
(C) uma consulta pode existir sem estar associada a um médico.  
(D) um médico pode não realizar consulta alguma.  
(E) uma mesma consulta pode ser realizada por diversos médicos.

---

**6**

Uma instituição de ensino modelou o relacionamento entre as entidades Aluno e Disciplina, no qual um aluno cursa várias disciplinas e uma disciplina é cursada por vários alunos. É necessário registrar a nota obtida por cada aluno em cada disciplina.

No modelo conceitual, a nota deve ser

(A) armazenada como atributo da entidade Aluno.  
(B) armazenada como atributo da entidade Disciplina.  
(C) associada ao relacionamento entre Aluno e Disciplina.  
(D) representada como atributo derivado da entidade Aluno.  
(E) omitida do modelo conceitual e criada apenas no modelo físico.

---

**7**

Em uma transportadora, todo funcionário é obrigatoriamente motorista ou administrativo, e nenhum funcionário pertence simultaneamente às duas categorias.

Essa especialização é classificada como

(A) parcial e exclusiva.  
(B) parcial e compartilhada.  
(C) total e exclusiva.  
(D) total e compartilhada.  
(E) uma agregação entre a entidade Funcionário e suas categorias.

---

**8**

No modelo conceitual de um sistema de gestão de pessoas, registrou-se que um empregado supervisiona outros empregados e que todo empregado, exceto o presidente, é supervisionado por um único empregado.

Esse tipo de construção é denominado

(A) relacionamento ternário.  
(B) autorrelacionamento.  
(C) agregação.  
(D) especialização.  
(E) relacionamento identificador.

---

**9**

Uma indústria precisa registrar a quantidade de peças que cada fornecedor entrega de cada produto para cada projeto. A quantidade só faz sentido quando se conhecem, simultaneamente, o fornecedor, o produto e o projeto.

A modelagem conceitual mais adequada para esse requisito consiste em

(A) três relacionamentos binários independentes entre as entidades envolvidas.  
(B) um relacionamento ternário entre Fornecedor, Produto e Projeto.  
(C) uma generalização que tenha Produto como superclasse.  
(D) uma entidade fraca dependente da entidade Produto.  
(E) um atributo multivalorado na entidade Projeto.

---

**10**

Em um sistema hospitalar, o relacionamento Consulta, estabelecido entre Médico e Paciente, precisa, por sua vez, relacionar-se com a entidade Exame, pois os exames são solicitados em uma consulta específica.

O recurso do modelo E-R que permite que um relacionamento participe de outro relacionamento é a

(A) especialização.  
(B) agregação.  
(C) generalização.  
(D) dependência de identificação.  
(E) cardinalidade máxima.

---

**11**

Considere um modelo conceitual em que um departamento possui vários empregados e cada empregado está lotado em um único departamento.

Na transformação para o modelo lógico relacional, esse relacionamento deve ser representado pela

(A) criação de uma tabela específica para o relacionamento, com chave composta.  
(B) inclusão da chave primária de Departamento como chave estrangeira em Empregado.  
(C) inclusão da chave primária de Empregado como chave estrangeira em Departamento.  
(D) fusão das duas entidades em uma única tabela.  
(E) definição de um atributo multivalorado na tabela Departamento.

---

**12**

Uma editora modelou o relacionamento entre Autor e Livro, em que um autor escreve vários livros e um livro pode ser escrito por vários autores.

A transformação desse relacionamento para o modelo lógico relacional gera

(A) duas tabelas, com chave estrangeira em Livro.  
(B) duas tabelas, com chave estrangeira em Autor.  
(C) três tabelas, sendo uma delas com chave primária composta pelas chaves das outras duas.  
(D) uma única tabela, contendo os atributos de autores e de livros.  
(E) três tabelas, sendo que a terceira não possui chave estrangeira.

---

**13**

Em uma empresa, todo crachá corporativo pertence a exatamente um empregado, mas nem todo empregado possui crachá.

A representação mais adequada desse relacionamento no modelo lógico relacional consiste em

(A) incluir a chave de Cracha como chave estrangeira em Empregado, permitindo valores nulos.  
(B) incluir a chave de Empregado como chave estrangeira em Cracha, com restrição de unicidade.  
(C) criar uma tabela associativa entre Empregado e Cracha.  
(D) fundir Empregado e Cracha em uma única tabela com colunas opcionais.  
(E) replicar as chaves primárias nas duas tabelas, sem chave estrangeira.

---

**14**

A entidade fraca Dependente é identificada pelo atributo nome, em conjunto com a entidade forte Segurado, cuja chave primária é o número da apólice.

No modelo lógico relacional, a chave primária da tabela Dependente é

(A) formada apenas pelo atributo nome.  
(B) composta pelo atributo nome e pela chave primária de Segurado.  
(C) formada apenas pela chave primária de Segurado.  
(D) obrigatoriamente uma chave substituta gerada pelo SGBD.  
(E) qualquer atributo da tabela que não admita valor nulo.

---

**15**

Uma seguradora modelou a superclasse Apólice e as subclasses ApóliceVida e ApóliceAuto, cada uma com atributos específicos, além dos atributos comuns herdados.

Uma estratégia válida de mapeamento dessa hierarquia para o modelo lógico relacional consiste em

(A) criar uma única tabela com os atributos comuns e os específicos, admitindo colunas opcionais.  
(B) criar tabelas apenas para as subclasses, eliminando obrigatoriamente os atributos comuns.  
(C) criar tabela apenas para a superclasse, descartando os atributos específicos das subclasses.  
(D) criar uma tabela distinta para cada atributo especializado das subclasses.  
(E) representar as subclasses como atributos multivalorados da superclasse.

---

**16**

No modelo relacional, o grau de uma relação corresponde ao número de

(A) tuplas existentes na relação.  
(B) atributos que compõem a relação.  
(C) chaves candidatas identificadas na relação.  
(D) restrições de integridade aplicadas à relação.  
(E) domínios distintos referenciados pela relação.

---

**17**

Na tabela Funcionário, os atributos CPF e Matrícula identificam unicamente cada registro. A equipe de projeto definiu Matrícula como chave primária.

Nesse caso, o CPF é classificado como chave

(A) estrangeira.  
(B) alternativa.  
(C) composta.  
(D) parcial.  
(E) artificial.

---

**18**

Um administrador de banco de dados criou um índice sobre a coluna data_emissao de uma tabela de notas fiscais, sem que fosse necessário alterar as aplicações que consultam essa tabela.

Essa situação exemplifica a independência de dados

(A) lógica.  
(B) física.  
(C) referencial.  
(D) semântica.  
(E) transacional.

---

**19**

Ao longo do projeto de um banco de dados, diferentes decisões são tomadas em cada nível de abstração.

Pertence exclusivamente ao projeto físico do banco de dados a

(A) definição das entidades e de seus relacionamentos.  
(B) escolha dos atributos identificadores de cada entidade.  
(C) criação de índices e definição da forma de armazenamento das tabelas.  
(D) aplicação das formas normais sobre as relações obtidas.  
(E) determinação das cardinalidades mínima e máxima dos relacionamentos.

---

**20**

Uma empresa assumiu a manutenção de um sistema legado cujo banco de dados está em produção há quinze anos, sem qualquer documentação de projeto. A equipe precisa obter os modelos de dados correspondentes ao esquema existente.

O processo adequado para essa finalidade é denominado

(A) engenharia reversa.  
(B) normalização.  
(C) modelagem dimensional.  
(D) refatoração conceitual.  
(E) tuning de banco de dados.