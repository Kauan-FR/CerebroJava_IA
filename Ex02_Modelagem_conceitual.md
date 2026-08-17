---
Data: 2026-08-17
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
**1**

Uma equipe concluiu o modelo lógico de um banco de dados e iniciou a construção do modelo físico.

Nessa transição, é decisão que pertence **exclusivamente** ao modelo físico a

- [ ] (A) definição das chaves primárias de cada tabela.  
- [ ] (B) aplicação das formas normais sobre as relações.  
- [x] (C) escolha do tablespace em que cada tabela será armazenada.  
- [ ] (D) determinação das chaves estrangeiras entre as tabelas.  
- [ ] (E) nomeação das colunas de acordo com o padrão corporativo.

---

**2**

A tabela `Cliente` já contém 40.000 registros quando um analista executa o comando a seguir.

sql

```sql
ALTER TABLE Cliente
ADD email VARCHAR(80) NOT NULL;
```

Para que esse comando seja executado com sucesso, é necessário

- [ ] (A) remover previamente a chave primária da tabela.  
- [ ] (B) especificar um valor padrão (DEFAULT) para a nova coluna.  
- [ ] (C) converter a tabela para uma estrutura particionada.  
- [x] (D) criar um índice sobre a nova coluna antes da alteração.  
- [ ] (E) executar o comando dentro de uma transação com isolamento serializável.

---

**3**

Considere a definição a seguir, criada no modelo físico de um sistema de pedidos.

sql

```sql
CREATE TABLE ItemPedido (
  id_pedido  INTEGER,
  id_produto INTEGER,
  quantidade INTEGER,
  PRIMARY KEY (id_pedido, id_produto),
  FOREIGN KEY (id_pedido) REFERENCES Pedido(id_pedido)
    ON DELETE CASCADE
);
```

A cláusula `ON DELETE CASCADE` determina que, ao se excluir um pedido,

- [ ] (A) a exclusão seja bloqueada caso existam itens associados.  
- [x] (B) os itens associados a esse pedido sejam também excluídos.  
- [ ] (C) a chave estrangeira dos itens associados receba valor nulo.  
- [ ] (D) a chave estrangeira dos itens associados receba o valor padrão.  
- [ ] (E) os itens associados sejam transferidos para um pedido genérico.

---

**4**

Ao criar a tabela `Funcionario`, um projetista definiu `matricula` como chave primária e aplicou a restrição UNIQUE sobre a coluna `cpf`.

Uma diferença entre essas duas restrições é que a restrição UNIQUE

- [ ] (A) impede a criação de índices sobre a coluna.  
- [x] (B) admite, conforme o padrão SQL, a ocorrência de valor nulo.  
- [ ] (C) só pode ser aplicada a colunas de tipo numérico.  
- [ ] (D) não é verificada durante operações de atualização.  
- [ ] (E) obriga a existência de uma chave estrangeira correspondente.

---

**5**

Após medir o tempo de resposta dos relatórios gerenciais, uma equipe decidiu incluir, na tabela `Pedido`, a coluna `nome_cliente`, que já existe na tabela `Cliente`.

Essa alteração no modelo físico caracteriza

- [ ] (A) normalização.  
- [x] (B) desnormalização.  
- [ ] (C) engenharia reversa.  
- [ ] (D) integridade referencial.  
- [ ] (E) particionamento horizontal.

---

**6**

Um DBA criou um índice sobre a coluna `data_emissao` da tabela `NotaFiscal`, que recebe grande volume de inserções diárias.

Um efeito colateral esperado dessa criação é o(a)

- [ ] (A) aumento do tempo necessário para operações de inserção e atualização.  
- [ ] (B) impossibilidade de executar consultas que não utilizem essa coluna.  
- [ ] (C) perda da integridade referencial entre NotaFiscal e Cliente.  
- [ ] (D) conversão automática da tabela para o modelo dimensional.  
- [x] (E) redução do espaço total ocupado pelo banco de dados.

---

**7**

Um sistema legado acessa diretamente a tabela `Empregado`. A equipe precisa reorganizar essa tabela em duas, sem alterar as aplicações existentes.

O recurso adequado para preservar o acesso das aplicações é a criação de

- [ ] (A) um índice composto sobre as duas novas tabelas.  
- [x] (B) uma visão (view) com a estrutura original da tabela.  
- [ ] (C) uma restrição CHECK sobre as colunas migradas.  
- [ ] (D) uma sequência para geração das novas chaves primárias.  
- [ ] (E) um gatilho de auditoria sobre as tabelas resultantes.

---

**8**

Considere as tabelas `Departamento` e `Empregado`, em que `Empregado.id_departamento` é chave estrangeira que referencia `Departamento.id_departamento`.

A tentativa de executar `DROP TABLE Departamento` resultará em

- [ ] (A) sucesso, com a remoção automática da tabela Empregado.  
- [ ] (B) sucesso, com a conversão da chave estrangeira em coluna comum.  
- [x] (C) erro, em razão da dependência gerada pela chave estrangeira.  
- [ ] (D) erro, pois tabelas referenciadas não podem ser removidas em hipótese alguma.  
- [ ] (E) sucesso, com a atribuição de valor nulo à coluna id_departamento.

---

**9**

Durante a construção do modelo lógico de um sistema de vendas, verificou-se que a chave natural candidata para identificar produtos é o código do fabricante, sujeito a mudanças frequentes e composto por quinze caracteres.

Nesse cenário, recomenda-se adotar uma chave

- [ ] (A) estrangeira, replicando o código nas tabelas relacionadas.  
- [x] (B) parcial, formada apenas pelos cinco primeiros caracteres.  
- [ ] (C) substituta (surrogate), gerada e controlada pelo próprio sistema.  
- [ ] (D) alternativa, eliminando-se a chave primária da tabela.  
- [ ] (E) composta, unindo o código do fabricante à data de cadastro.

---

**10**

Ao definir a tabela `Conta`, a equipe precisa garantir que a coluna `tipo` aceite somente os valores 'CORRENTE' e 'POUPANCA'.

A restrição adequada para esse requisito é

- [ ] (A) NOT NULL.  
- [ ] (B) UNIQUE.  
- [ ] (C) CHECK.  
- [ ] (D) PRIMARY KEY.  
- [ ] (E) FOREIGN KEY.

---

**11**

Uma consultoria recebeu apenas os scripts de criação das tabelas de um sistema em produção e precisa obter o diagrama entidade-relacionamento correspondente.

O processo utilizado, nesse caso, parte do modelo

(A) físico em direção ao conceitual, sendo denominado engenharia reversa.  
(B) conceitual em direção ao físico, sendo denominado engenharia reversa.  
(C) físico em direção ao conceitual, sendo denominado forward engineering.  
(D) lógico em direção ao físico, sendo denominado normalização.  
(E) conceitual em direção ao lógico, sendo denominado refatoração.

---

**12**

A coluna `sigla` da tabela `Estado` foi criada como VARCHAR(10) e contém valores de até 8 caracteres. Um analista pretende executar a alteração a seguir.

sql

```sql
ALTER TABLE Estado
ALTER COLUMN sigla TYPE VARCHAR(2);
```

O resultado esperado dessa execução é

(A) sucesso, com truncamento silencioso dos valores existentes.  
(B) sucesso, com preservação integral dos valores existentes.  
(C) erro, pois existem valores incompatíveis com o novo tamanho.  
(D) erro, pois o tipo VARCHAR não admite redução de tamanho.  
(E) sucesso, com conversão automática dos valores para CHAR(2).

---

**13**

Uma equipe discute em que medida o modelo lógico depende da tecnologia adotada.

O modelo lógico caracteriza-se por ser

(A) totalmente independente de qualquer modelo de dados.  
(B) dependente do produto de SGBD escolhido pela organização.  
(C) dependente do modelo de dados adotado, porém independente do produto de SGBD.  
(D) dependente da estrutura de armazenamento definida em disco.  
(E) idêntico ao modelo conceitual, diferindo apenas na notação gráfica.

---

**14**

A tabela `Movimentacao` armazena dez anos de lançamentos, e as consultas mais frequentes recuperam apenas os registros do ano corrente.

A técnica de modelo físico indicada para esse cenário é o(a)

(A) particionamento da tabela por faixa de datas.  
(B) criação de uma restrição CHECK sobre a data.  
(C) normalização até a Terceira Forma Normal.  
(D) substituição da chave primária por chave composta.  
(E) criação de uma tabela associativa para os lançamentos antigos.

---

**15**

Um analista renomeou a tabela `Cliente` para `ClientePessoaFisica` no modelo físico de um sistema em produção.

Uma consequência direta dessa alteração é que

(A) todas as chaves estrangeiras da base são automaticamente removidas.  
(B) objetos dependentes, como visões e procedimentos, podem tornar-se inválidos.  
(C) os dados armazenados na tabela são perdidos durante a operação.  
(D) o modelo conceitual é atualizado automaticamente pelo SGBD.  
(E) os índices existentes precisam ser recriados manualmente em qualquer SGBD.

---

**16**

Durante a criação de uma tabela, definiu-se que a coluna `data_admissao` não pode receber valor nulo e que a coluna `salario` deve ser sempre maior que zero.

As restrições que atendem, respectivamente, a esses requisitos são

(A) CHECK e NOT NULL.  
(B) NOT NULL e CHECK.  
(C) NOT NULL e UNIQUE.  
(D) UNIQUE e CHECK.  
(E) DEFAULT e NOT NULL.

---

**17**

Ao executar comandos de criação e alteração de tabelas, o SGBD registra automaticamente as informações sobre as estruturas criadas.

Essas informações são armazenadas no(a)

(A) log de transações.  
(B) catálogo do sistema (dicionário de dados).  
(C) plano de execução das consultas.  
(D) área de buffer do SGBD.  
(E) arquivo de backup incremental.

---

**18**

Um relacionamento N:M entre `Aluno` e `Disciplina` foi implementado por meio da tabela `Matricula`, cuja chave primária é composta pelas chaves das duas tabelas. Passou-se a exigir o registro da data de matrícula.

Para atender a esse novo requisito, deve-se

(A) criar uma nova tabela associativa entre Matricula e Disciplina.  
(B) acrescentar a coluna data_matricula à tabela Matricula.  
(C) acrescentar a coluna data_matricula à tabela Aluno.  
(D) incluir a data de matrícula na chave primária de Disciplina.  
(E) converter o relacionamento N:M em dois relacionamentos 1:N.

---

**19**

Um DBA criou o índice a seguir sobre a tabela `Venda`.

sql

```sql
CREATE INDEX idx_venda ON Venda (id_loja, data_venda);
```

Esse índice é aproveitado com maior eficiência por consultas que filtram

(A) apenas pela coluna data_venda.  
(B) pela coluna id_loja, isoladamente ou combinada com data_venda.  
(C) apenas por colunas que não integram o índice.  
(D) exclusivamente pelas duas colunas em conjunto, nunca isoladamente.  
(E) pela coluna data_venda, isoladamente ou combinada com id_loja.

---

**20**

Uma tabela precisa gerar valores numéricos únicos e sequenciais para sua chave primária, sem que a aplicação controle o último valor utilizado.

O recurso do modelo físico adequado a esse requisito é

(A) a restrição UNIQUE sobre a coluna.  
(B) a definição de uma coluna de identidade ou sequência (sequence).  
(C) a criação de uma visão materializada sobre a tabela.  
(D) o uso de uma restrição CHECK com valor incremental.  
(E) a criação de um índice do tipo bitmap sobre a coluna.