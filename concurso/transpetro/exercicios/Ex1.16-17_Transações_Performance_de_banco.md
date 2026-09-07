---
Data: 2026-09-07
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Uma transação, em um Sistema Gerenciador de Banco de Dados, é definida como

- [ ] (A) o conjunto de índices criados sobre uma tabela.  
- [x] (B) uma unidade lógica de trabalho, composta por uma ou mais operações, executada integralmente ou não executada.  
- [ ] (C) a estrutura de armazenamento adotada para os arquivos de dados.  
- [ ] (D) o plano de execução escolhido pelo otimizador de consultas.  
- [ ] (E) o conjunto de privilégios concedidos a um usuário do banco.

---

**2**

Um analista executou uma sequência de comandos `INSERT` e `UPDATE` e, ao constatar erro nos valores informados, precisou desfazer todas as alterações realizadas desde o início da transação.

O comando adequado a essa finalidade é

- [ ] (A) `COMMIT`  
- [x] (B) `ROLLBACK`  
- [ ] (C) `SAVEPOINT`  
- [ ] (D) `TRUNCATE`  
- [ ] (E) `REVOKE`

---

**3**

Em uma transação longa, um analista deseja marcar um ponto intermediário, de modo que seja possível desfazer apenas parte das operações, sem descartar a transação inteira.

O comando adequado a essa finalidade é

- [ ] (A) `COMMIT`  
- [ ] (B) `ROLLBACK`  
- [x] (C) `SAVEPOINT`  
- [ ] (D) `CHECKPOINT`  
- [ ] (E) `GRANT`

---

**4**

Uma transação T1 alterou o valor de uma linha e ainda não confirmou a operação. A transação T2 leu esse valor e, em seguida, T1 executou `ROLLBACK`.

O problema de concorrência caracterizado é a

- [x] (A) leitura suja (dirty read).  
- [ ] (B) leitura não repetível (non-repeatable read).  
- [ ] (C) leitura fantasma (phantom read).  
- [ ] (D) perda de atualização (lost update).  
- [ ] (E) violação de durabilidade.

---

**5**

Uma transação T1 leu o salário de um empregado, obtendo R$ 5.000,00. Em seguida, T2 alterou esse salário para R$ 6.000,00 e confirmou a operação. Ao reler a mesma linha, T1 obteve R$ 6.000,00.

O problema de concorrência caracterizado é a

- [ ] (A) leitura suja.  
- [x] (B) leitura não repetível.  
- [ ] (C) leitura fantasma.  
- [ ] (D) perda de atualização.  
- [ ] (E) escrita suja.

---

**6**

Uma transação T1 executou uma consulta que retornou 15 linhas. Em seguida, T2 inseriu novas linhas que atendem à mesma condição e confirmou a operação. Ao reexecutar a consulta, T1 obteve 18 linhas.

O problema de concorrência caracterizado é a

- [ ] (A) leitura suja.  
- [ ] (B) leitura não repetível.  
- [x] (C) leitura fantasma.  
- [ ] (D) perda de atualização.  
- [ ] (E) violação de atomicidade.

---

**7**

Considere os níveis de isolamento definidos pelo padrão SQL.

O nível que impede leitura suja e leitura não repetível, mas ainda admite leitura fantasma, é

- [ ] (A) READ UNCOMMITTED.  
- [ ] (B) READ COMMITTED.  
- [x] (C) REPEATABLE READ.  
- [ ] (D) SERIALIZABLE.  
- [ ] (E) DIRTY READ.

---

**8**

Duas transações aguardam, cada uma, a liberação de um recurso bloqueado pela outra, e nenhuma delas consegue prosseguir.

Essa situação é denominada

- [x] (A) impasse (deadlock).  
- [ ] (B) leitura fantasma.  
- [ ] (C) inanição de índice.  
- [ ] (D) fragmentação de tablespace.  
- [ ] (E) violação de consistência.

---

**9**

Um SGBD detectou um impasse entre duas transações concorrentes.

A providência usualmente adotada pelo SGBD nessa situação é

- [ ] (A) confirmar automaticamente ambas as transações.  
- [x] (B) abortar uma das transações envolvidas, desfazendo suas operações.  
- [ ] (C) suspender indefinidamente as duas transações até intervenção manual.  
- [ ] (D) converter as transações em consultas somente leitura.  
- [ ] (E) remover os índices das tabelas envolvidas.

---

**10**

Uma equipe identificou que determinada consulta apresenta tempo de resposta elevado e precisa compreender a estratégia adotada pelo SGBD para executá-la.

O recurso adequado a essa análise é

- [x] (A) o plano de execução gerado pelo otimizador.  
- [ ] (B) o log de transações do SGBD.  
- [ ] (C) o catálogo do sistema.  
- [ ] (D) o backup incremental do banco.  
- [ ] (E) a área de estágio do processo de ETL.

---

**11**

Um administrador criou um índice sobre a coluna `data_pedido` de uma tabela que recebe grande volume de inserções diárias.

Um efeito colateral esperado dessa criação é o(a)

- [ ] (A) aumento do tempo necessário para as operações de inserção e atualização.  
- [ ] (B) redução do espaço total ocupado pelo banco de dados.  
- [x] (C) impossibilidade de executar consultas sobre as demais colunas.  
- [ ] (D) perda da integridade referencial com as tabelas relacionadas.  
- [ ] (E) eliminação da necessidade de coleta de estatísticas.

---

**12**

Um administrador criou o índice a seguir sobre a tabela `Venda`.

sql

```sql
CREATE INDEX idx_venda ON Venda (id_loja, data_venda);
```

Esse índice é aproveitado com maior eficiência por consultas que filtram

- [ ] (A) apenas pela coluna data_venda.  
- [x] (B) pela coluna id_loja, isoladamente ou combinada com data_venda.  
- [ ] (C) apenas por colunas que não integram o índice.  
- [ ] (D) exclusivamente pelas duas colunas em conjunto, nunca isoladamente.  
- [ ] (E) pela coluna data_venda, isoladamente ou combinada com id_loja.

---

**13**

O otimizador de consultas de um SGBD relacional baseado em custo utiliza, para escolher o plano de execução, principalmente

- [x] (A) as estatísticas mantidas sobre a distribuição dos dados nas tabelas.  
- [ ] (B) a ordem em que as tabelas aparecem na cláusula FROM.  
- [ ] (C) a quantidade de caracteres da consulta submetida.  
- [ ] (D) o nível de isolamento configurado para a sessão.  
- [ ] (E) o conteúdo do log de transações.

---

**14**

Uma consulta executada sobre uma tabela de dez milhões de linhas apresenta, em seu plano de execução, a operação de varredura completa da tabela (_full table scan_), embora filtre por uma única coluna de alta seletividade.

A providência mais adequada para melhorar o desempenho dessa consulta é

- [x] (A) criar um índice sobre a coluna utilizada no filtro.  
- [ ] (B) aumentar o nível de isolamento da transação.  
- [ ] (C) converter a tabela para o modelo dimensional.  
- [ ] (D) remover as chaves estrangeiras da tabela.  
- [ ] (E) executar o comando TRUNCATE sobre a tabela.

---

**15**

Após medir a lentidão de relatórios que exigiam múltiplas junções, uma equipe decidiu reintroduzir, de forma controlada, dados redundantes em determinadas tabelas.

Essa decisão de projeto físico é denominada

- [ ] (A) normalização.  
- [x] (B) desnormalização.  
- [ ] (C) particionamento vertical.  
- [ ] (D) engenharia reversa.  
- [ ] (E) controle de concorrência otimista.

---

**16**

Uma tabela armazena quinze anos de lançamentos contábeis, e as consultas mais frequentes recuperam apenas os registros do exercício corrente.

A técnica de modelo físico indicada para esse cenário é o(a)

- [ ] (A) particionamento da tabela por faixa de datas.  
- [x] (B) criação de restrição CHECK sobre a coluna de data.  
- [ ] (C) normalização até a Forma Normal de Boyce-Codd.  
- [ ] (D) conversão da chave primária em chave composta.  
- [ ] (E) criação de uma dimensão degenerada.

---

**17**

Um analista precisa disponibilizar, para consultas analíticas frequentes, o resultado pré-calculado de uma consulta complexa que agrega milhões de linhas, admitindo-se que os dados sejam atualizados periodicamente.

O recurso adequado a essa finalidade é a criação de

- [ ] (A) uma visão comum (view).  
- [x] (B) uma visão materializada.  
- [ ] (C) um gatilho de auditoria.  
- [ ] (D) uma sequência (sequence).  
- [ ] (E) uma restrição UNIQUE.

---

**18**

Uma consulta utiliza a expressão a seguir em sua cláusula WHERE.

sql

```sql
WHERE UPPER(nome_cliente) = 'MARIA'
```

Existe um índice comum criado sobre a coluna `nome_cliente`.

Em relação a essa consulta, é correto afirmar que o índice

- [ ] (A) será utilizado normalmente, pois a coluna está indexada.  
- [x] (B) tende a não ser utilizado, pois a aplicação de função sobre a coluna impede o uso do índice comum.  
- [ ] (C) será convertido automaticamente em índice composto pelo SGBD.  
- [ ] (D) impedirá a execução da consulta, por incompatibilidade de tipo.  
- [ ] (E) provocará a recriação automática das estatísticas da tabela.

---

**19**

O uso de índices em bancos de dados relacionais envolve benefícios e custos.

**NÃO** constitui custo associado à criação de um índice a

- [ ] (A) ocupação adicional de espaço em disco.  
- [ ] (B) sobrecarga nas operações de inserção, atualização e exclusão.  
- [x] (C) necessidade de manutenção e reorganização periódica.  
- [ ] (D) redução do tempo de resposta das consultas que utilizam a coluna indexada.  
- [ ] (E) esforço adicional do otimizador na avaliação dos planos disponíveis.

---

**20**

Um analista relacionou providências para melhoria de desempenho de um banco de dados relacional.

**NÃO** constitui técnica de melhoria de desempenho a

- [ ] (A) criação de índices sobre colunas frequentemente utilizadas em filtros.  
- [ ] (B) particionamento de tabelas de grande volume.  
- [ ] (C) atualização periódica das estatísticas utilizadas pelo otimizador.  
- [x] (D) remoção das restrições de integridade referencial declaradas.  
- [ ] (E) reescrita de consultas para evitar varreduras completas desnecessárias.