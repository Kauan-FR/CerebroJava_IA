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
<font color="#00b050">- [x] (C) escolha do tablespace em que cada tabela será armazenada.  </font>
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
<font color="#00b050">- [ ] (B) especificar um valor padrão (DEFAULT) para a nova coluna.  </font>
- [ ] (C) converter a tabela para uma estrutura particionada.  
<font color="#ff0000">- [x] (D) criar um índice sobre a nova coluna antes da alteração.  </font>
- [ ] (E) executar o comando dentro de uma transação com isolamento serializável.

>[!fail] Adicionar valores nas 40.000
>Criar índices é performance, não integração.
>Como os valores eles já estão lá e não poderemos retira-los, o melhor a se fazer é adicionar o `DEFALT` com informações padrões só para que a alteração seja feita.
>
>```sql
>ALTER TABLE Cliente
ADD email VARCHAR(80) NOT NULL DEFALT 'nao_informado';
>```

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
<font color="#00b050">- [x] (B) os itens associados a esse pedido sejam também excluídos.  </font>
- [ ] (C) a chave estrangeira dos itens associados receba valor nulo.  
- [ ] (D) a chave estrangeira dos itens associados receba o valor padrão.  
- [ ] (E) os itens associados sejam transferidos para um pedido genérico.

---

**4**

Ao criar a tabela `Funcionario`, um projetista definiu `matricula` como chave primária e aplicou a restrição UNIQUE sobre a coluna `cpf`.

Uma diferença entre essas duas restrições é que a restrição UNIQUE

- [ ] (A) impede a criação de índices sobre a coluna.  
<font color="#00b050">- [x] (B) admite, conforme o padrão SQL, a ocorrência de valor nulo.  </font>
- [ ] (C) só pode ser aplicada a colunas de tipo numérico.  
- [ ] (D) não é verificada durante operações de atualização.  
- [ ] (E) obriga a existência de uma chave estrangeira correspondente.

---

**5**

Após medir o tempo de resposta dos relatórios gerenciais, uma equipe decidiu incluir, na tabela `Pedido`, a coluna `nome_cliente`, que já existe na tabela `Cliente`.

Essa alteração no modelo físico caracteriza

- [ ] (A) normalização.  
<font color="#00b050">- [x] (B) desnormalização.  </font>
- [ ] (C) engenharia reversa.  
- [ ] (D) integridade referencial.  
- [ ] (E) particionamento horizontal.

---

**6**

Um DBA criou um índice sobre a coluna `data_emissao` da tabela `NotaFiscal`, que recebe grande volume de inserções diárias.

Um efeito colateral esperado dessa criação é o(a)

<font color="#00b050">- [ ] (A) aumento do tempo necessário para operações de inserção e atualização.  </font>
- [ ] (B) impossibilidade de executar consultas que não utilizem essa coluna.  
- [ ] (C) perda da integridade referencial entre NotaFiscal e Cliente.  
- [ ] (D) conversão automática da tabela para o modelo dimensional.  
<font color="#ff0000">- [x] (E) redução do espaço total ocupado pelo banco de dados.</font>

>[!fail] O custo do índice
>O índice ele ocupa espaço a mais na memória, e acelera a leitura e **desacelera escrita**, porque cada `INSERT`, `DELETE` e `UPDATE` precisa atualizar a tabela, e também o índice.
>O uso do índice é uma troca
>
>| Ganha | Consequência|
>|:-----:|:----:|
>|Leitura mais rápida|Escrita mais lenta|
>||Espaço em disco|
>||Manutenção pelo SGBD|

---

**7**

Um sistema legado acessa diretamente a tabela `Empregado`. A equipe precisa reorganizar essa tabela em duas, sem alterar as aplicações existentes.

O recurso adequado para preservar o acesso das aplicações é a criação de

- [ ] (A) um índice composto sobre as duas novas tabelas.  
<font color="#00b050">- [x] (B) uma visão (view) com a estrutura original da tabela.  </font>
- [ ] (C) uma restrição CHECK sobre as colunas migradas.  
- [ ] (D) uma sequência para geração das novas chaves primárias.  
- [ ] (E) um gatilho de auditoria sobre as tabelas resultantes.

---

**8**

Considere as tabelas `Departamento` e `Empregado`, em que `Empregado.id_departamento` é chave estrangeira que referencia `Departamento.id_departamento`.

A tentativa de executar `DROP TABLE Departamento` resultará em

- [ ] (A) sucesso, com a remoção automática da tabela Empregado.  
- [ ] (B) sucesso, com a conversão da chave estrangeira em coluna comum.  
<font color="#00b050">- [x] (C) erro, em razão da dependência gerada pela chave estrangeira.  </font>
- [ ] (D) erro, pois tabelas referenciadas não podem ser removidas em hipótese alguma.  
- [ ] (E) sucesso, com a atribuição de valor nulo à coluna id_departamento.

---

**9**

Durante a construção do modelo lógico de um sistema de vendas, verificou-se que a chave natural candidata para identificar produtos é o código do fabricante, sujeito a mudanças frequentes e composto por quinze caracteres.

Nesse cenário, recomenda-se adotar uma chave

- [ ] (A) estrangeira, replicando o código nas tabelas relacionadas.  
<font color="#ff0000">- [x] (B) parcial, formada apenas pelos cinco primeiros caracteres.  </font>
<font color="#00b050">- [ ] (C) substituta (surrogate), gerada e controlada pelo próprio sistema.  </font>
- [ ] (D) alternativa, eliminando-se a chave primária da tabela.  
- [ ] (E) composta, unindo o código do fabricante à data de cadastro.

>[!fail] Chave substituta(surrogate)
>Os defeitos listados no enunciado da chave primaria é um problema, porque a chave não esta fazendo a sua função que é ter os dados imutáveis
>A solução para esse problema é **substituir a chave, e criar outra no lugar dela**

---

**10**

Ao definir a tabela `Conta`, a equipe precisa garantir que a coluna `tipo` aceite somente os valores 'CORRENTE' e 'POUPANCA'.

A restrição adequada para esse requisito é

<font color="#ff0000">- [x] (A) NOT NULL.  </font>
- [ ] (B) UNIQUE.  
<font color="#00b050">- [ ] (C) CHECK.  </font>
- [ ] (D) PRIMARY KEY.  
- [ ] (E) FOREIGN KEY.

>[!fail] CHECK
>O `NOT NULL` ele impede que o valor seja nulo, **não que ele seja um ou outro**, pois ele pode aceitar outros valores diferentes, além dos que o enunciado pede, **porque ele só impede que o valor não seja nulo e mais nada**
>Mas o `CHECK` ele **limita quais valores a tabela pode aceitar**
>```sql
>tipo VARCHAR(10) CHECK (tipo IN ('CORRENTE','POUPANCA'))
>```

---

**11**

Uma consultoria recebeu apenas os scripts de criação das tabelas de um sistema em produção e precisa obter o diagrama entidade-relacionamento correspondente.

O processo utilizado, nesse caso, parte do modelo

<font color="#00b050">- [x] (A) físico em direção ao conceitual, sendo denominado engenharia reversa.  </font>
- [ ] (B) conceitual em direção ao físico, sendo denominado engenharia reversa.  
- [ ] (C) físico em direção ao conceitual, sendo denominado forward engineering.  
- [ ] (D) lógico em direção ao físico, sendo denominado normalização.  
- [ ] (E) conceitual em direção ao lógico, sendo denominado refatoração.

---

**12**

A coluna `sigla` da tabela `Estado` foi criada como VARCHAR(10) e contém valores de até 8 caracteres. Um analista pretende executar a alteração a seguir.

sql

```sql
ALTER TABLE Estado
ALTER COLUMN sigla TYPE VARCHAR(2);
```

O resultado esperado dessa execução é

- [ ] (A) sucesso, com truncamento silencioso dos valores existentes.  
- [ ] (B) sucesso, com preservação integral dos valores existentes.  
<font color="#00b050">- [x] (C) erro, pois existem valores incompatíveis com o novo tamanho.  </font>
- [ ] (D) erro, pois o tipo VARCHAR não admite redução de tamanho.  
- [ ] (E) sucesso, com conversão automática dos valores para CHAR(2).

---

**13**

Uma equipe discute em que medida o modelo lógico depende da tecnologia adotada.

O modelo lógico caracteriza-se por ser

- [ ] (A) totalmente independente de qualquer modelo de dados.  
- [ ] (B) dependente do produto de SGBD escolhido pela organização.  
<font color="#00b050">- [x] (C) dependente do modelo de dados adotado, porém independente do produto de SGBD.  </font>
- [ ] (D) dependente da estrutura de armazenamento definida em disco.  
- [ ] (E) idêntico ao modelo conceitual, diferindo apenas na notação gráfica.

---

**14**

A tabela `Movimentacao` armazena dez anos de lançamentos, e as consultas mais frequentes recuperam apenas os registros do ano corrente.

A técnica de modelo físico indicada para esse cenário é o(a)

<font color="#00b050">- [x] (A) particionamento da tabela por faixa de datas.  </font>
- [ ] (B) criação de uma restrição CHECK sobre a data.  
- [ ] (C) normalização até a Terceira Forma Normal.  
- [ ] (D) substituição da chave primária por chave composta.  
- [ ] (E) criação de uma tabela associativa para os lançamentos antigos.

---

**15**

Um analista renomeou a tabela `Cliente` para `ClientePessoaFisica` no modelo físico de um sistema em produção.

Uma consequência direta dessa alteração é que

- [ ] (A) todas as chaves estrangeiras da base são automaticamente removidas.  
<font color="#00b050">- [ ] (B) objetos dependentes, como visões e procedimentos, podem tornar-se inválidos.  </font>
- [ ] (C) os dados armazenados na tabela são perdidos durante a operação.  
<font color="#ff0000">- [x] (D) o modelo conceitual é atualizado automaticamente pelo SGBD.  </font>
- [ ] (E) os índices existentes precisam ser recriados manualmente em qualquer SGBD.

>[!fail] Efeito colateral de renomear tabela
>O fato de renomear uma tabela não apaga dados ou remove chave estrangeira, **mas tudo que referencia a tabela pelo nome quebra** como, visões, procedimentos armazenados, funções, gatilhos.

---

**16**

Durante a criação de uma tabela, definiu-se que a coluna `data_admissao` não pode receber valor nulo e que a coluna `salario` deve ser sempre maior que zero.

As restrições que atendem, respectivamente, a esses requisitos são

- [ ] (A) CHECK e NOT NULL.  
<font color="#00b050">- [x] (B) NOT NULL e CHECK.  </font>
- [ ] (C) NOT NULL e UNIQUE.  
- [ ] (D) UNIQUE e CHECK.  
- [ ] (E) DEFAULT e NOT NULL.

---

**17**

Ao executar comandos de criação e alteração de tabelas, o SGBD registra automaticamente as informações sobre as estruturas criadas.

Essas informações são armazenadas no(a)

<font color="#ff0000">- [x] (A) log de transações.  </font>
<font color="#00b050">- [ ] (B) catálogo do sistema (dicionário de dados).  </font>
- [ ] (C) plano de execução das consultas.  
- [ ] (D) área de buffer do SGBD.  
- [ ] (E) arquivo de backup incremental.

>[!fail] Catálogo do sistema x log de transações
>||Guarda|Serve para|
|---|---|---|
|**Catálogo / dicionário de dados**|**Metadados**: tabelas, colunas, tipos, índices, restrições, usuários, permissões|Saber **como o banco é estruturado**|
|**Log de transações**|**Registro das operações**: o que foi alterado, quando, por qual transação|**Recuperar** o banco após falha, desfazer transação|
>
>Quando o enunciado falar em "informações sobre as **estruturas criadas**" - **estrutura é metadado**, logo **metadado** 

---

**18**

Um relacionamento N:M entre `Aluno` e `Disciplina` foi implementado por meio da tabela `Matricula`, cuja chave primária é composta pelas chaves das duas tabelas. Passou-se a exigir o registro da data de matrícula.

Para atender a esse novo requisito, deve-se

- [ ] (A) criar uma nova tabela associativa entre Matricula e Disciplina.  
<font color="#00b050">- [x] (B) acrescentar a coluna data_matricula à tabela Matricula.  </font>
- [ ] (C) acrescentar a coluna data_matricula à tabela Aluno.  
- [ ] (D) incluir a data de matrícula na chave primária de Disciplina.  
- [ ] (E) converter o relacionamento N:M em dois relacionamentos 1:N.

---

**19**

Um DBA criou o índice a seguir sobre a tabela `Venda`.

sql

```sql
CREATE INDEX idx_venda ON Venda (id_loja, data_venda);
```

Esse índice é aproveitado com maior eficiência por consultas que filtram

- [ ] (A) apenas pela coluna data_venda.  
<font color="#00b050">- [ ] (B) pela coluna id_loja, isoladamente ou combinada com data_venda.  </font>
- [ ] (C) apenas por colunas que não integram o índice.  
- [ ] (D) exclusivamente pelas duas colunas em conjunto, nunca isoladamente.  
<font color="#ff0000">- [x] (E) pela coluna data_venda, isoladamente ou combinada com id_loja.</font>

---

**20**

Uma tabela precisa gerar valores numéricos únicos e sequenciais para sua chave primária, sem que a aplicação controle o último valor utilizado.

O recurso do modelo físico adequado a esse requisito é

- [x] (A) a restrição UNIQUE sobre a coluna.  
- [ ] (B) a definição de uma coluna de identidade ou sequência (sequence).  
- [ ] (C) a criação de uma visão materializada sobre a tabela.  
- [ ] (D) o uso de uma restrição CHECK com valor incremental.  
- [ ] (E) a criação de um índice do tipo bitmap sobre a coluna.