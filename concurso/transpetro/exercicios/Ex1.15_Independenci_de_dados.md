---
Data: 2026-09-07
tags:
  - transpetro
  - exercicio
Tipo:
---
---

**1**

A arquitetura de três níveis proposta pelo ANSI/SPARC organiza a descrição de um banco de dados nos níveis

- [ ] (A) conceitual, lógico e físico.  
- [x] (B) externo, conceitual e interno.  
- [ ] (C) dimensional, relacional e hierárquico.  
- [ ] (D) operacional, tático e estratégico.  
- [ ] (E) transacional, analítico e distribuído.

---

**2**

Na arquitetura de três níveis, o nível que descreve como os dados estão efetivamente armazenados, incluindo estruturas de arquivos, índices e métodos de acesso, é o nível

- [ ] (A) externo.  
- [ ] (B) conceitual.  
- [x] (C) interno.  
- [ ] (D) semântico.  
- [ ] (E) dimensional.

---

**3**

Na arquitetura de três níveis, o nível que apresenta a visão particular de cada grupo de usuários sobre o banco de dados, ocultando as demais informações, é o nível

- [x] (A) externo.  
- [ ] (B) conceitual.  
- [ ] (C) interno.  
- [ ] (D) físico.  
- [ ] (E) transacional.

---

**4**

Um administrador de banco de dados criou um índice sobre a coluna `data_emissao` da tabela `NotaFiscal`, sem que fosse necessário alterar qualquer aplicação que consulta essa tabela.

Essa situação exemplifica a independência de dados

- [ ] (A) lógica.  
- [x] (B) física.  
- [ ] (C) referencial.  
- [ ] (D) semântica.  
- [ ] (E) transacional.

---

**5**

Uma equipe acrescentou a coluna `email_secundario` à tabela `Cliente`. As aplicações existentes, que não utilizam essa coluna, continuaram funcionando sem qualquer alteração.

Essa situação exemplifica a independência de dados

- [x] (A) lógica.  
- [ ] (B) física.  
- [ ] (C) física e lógica, simultaneamente.  
- [ ] (D) de domínio.  
- [ ] (E) de entidade.

---

**6**

A independência de dados física caracteriza-se pela possibilidade de alterar o esquema

- [x] (A) interno sem alterar o esquema conceitual nem as aplicações.  
- [ ] (B) conceitual sem alterar o esquema interno.  
- [ ] (C) externo sem alterar as visões dos usuários.  
- [ ] (D) conceitual sem alterar as regras de negócio da aplicação.  
- [ ] (E) interno mediante reescrita obrigatória das aplicações.

---

**7**

A independência de dados lógica caracteriza-se pela possibilidade de alterar o esquema

- [ ] (A) interno sem alterar o esquema conceitual.  
- [ ] (B) conceitual sem alterar os esquemas externos nem as aplicações.  
- [x] (C) externo sem alterar o esquema interno.  
- [ ] (D) físico sem alterar os índices existentes.  
- [ ] (E) conceitual mediante reorganização obrigatória dos arquivos em disco.

---

**8**

Segundo a literatura de banco de dados, a independência de dados lógica é considerada mais difícil de alcançar do que a independência física porque

- [ ] (A) o nível interno é gerenciado diretamente pelas aplicações.  
- [x] (B) as aplicações costumam depender diretamente da estrutura lógica dos dados que manipulam.  
- [ ] (C) os índices precisam ser recriados a cada alteração conceitual.  
- [ ] (D) o nível externo não pode ser modificado após a criação do banco.  
- [ ] (E) o SGBD não mantém mapeamento entre os níveis conceitual e interno.

---

**9**

Um sistema legado acessa diretamente a tabela `Empregado`. A equipe precisa dividir essa tabela em duas, sem alterar as aplicações existentes.

O recurso adequado para preservar o acesso das aplicações é a criação de

- [ ] (A) um índice composto sobre as duas novas tabelas.  
- [x] (B) uma visão (view) com a estrutura original da tabela.  
- [ ] (C) uma restrição CHECK sobre as colunas migradas.  
- [ ] (D) uma sequência para geração das novas chaves primárias.  
- [ ] (E) um gatilho de auditoria sobre as tabelas resultantes.

---

**10**

As visões (views) desempenham papel relevante na arquitetura de banco de dados porque

- [ ] (A) armazenam fisicamente cópias dos dados das tabelas de origem.  
- [x] (B) implementam o nível externo, sustentando a independência de dados lógica.  
- [ ] (C) substituem as restrições de integridade referencial declaradas.  
- [ ] (D) eliminam a necessidade de índices sobre as tabelas consultadas.  
- [ ] (E) impedem a execução de operações de junção entre tabelas.

---

**11**

Um administrador migrou os arquivos de dados de uma tabela para um novo dispositivo de armazenamento, mais rápido, mantendo inalterada a estrutura das tabelas.

Em relação às aplicações que consultam essa tabela, essa alteração

- [ ] (A) exigirá a reescrita das consultas SQL executadas.  
- [x] (B) não produzirá qualquer impacto, em razão da independência de dados física.  
- [ ] (C) exigirá a recriação de todas as visões existentes.  
- [ ] (D) invalidará as restrições de integridade referencial declaradas.  
- [ ] (E) exigirá a renormalização das tabelas envolvidas.

---

**12**

Na arquitetura de três níveis, o SGBD mantém correspondências que permitem traduzir requisições formuladas em um nível para outro.

Essas correspondências são denominadas

- [x] (A) mapeamentos.  
- [ ] (B) restrições de integridade.  
- [ ] (C) planos de execução.  
- [ ] (D) dependências funcionais.  
- [ ] (E) chaves substitutas.

---

**13**

Uma organização adotou o particionamento horizontal da tabela `Movimentacao`, distribuindo suas linhas em segmentos por ano. As consultas das aplicações permaneceram inalteradas.

Essa situação exemplifica a independência de dados

- [x] (A) lógica, pois alterou-se a estrutura das tabelas.  
- [ ] (B) física, pois alterou-se apenas a forma de armazenamento.  
- [ ] (C) semântica, pois alterou-se o significado dos dados.  
- [ ] (D) referencial, pois preservaram-se as chaves estrangeiras.  
- [ ] (E) externa, pois alteraram-se as visões dos usuários.

---

**14**

Diferentes grupos de usuários acessam o mesmo banco de dados corporativo. A equipe de folha de pagamento visualiza os salários dos empregados; a equipe de portaria visualiza apenas nome e matrícula.

Essa configuração é implementada no nível

- [ ] (A) interno, mediante particionamento físico.  
- [x] (B) externo, mediante visões distintas sobre o mesmo esquema conceitual.  
- [ ] (C) conceitual, mediante duplicação das tabelas de origem.  
- [ ] (D) transacional, mediante controle de concorrência.  
- [ ] (E) dimensional, mediante dimensões conformadas.

---

**15**

Em um banco de dados, o esquema conceitual descreve

- [ ] (A) as estruturas de arquivos e os métodos de acesso utilizados em disco.  
- [x] (B) a estrutura lógica global do banco, com entidades, atributos e relacionamentos, sem detalhes de armazenamento.  
- [ ] (C) a visão parcial de cada aplicação sobre os dados disponíveis.  
- [ ] (D) o plano de execução escolhido pelo otimizador de consultas.  
- [ ] (E) as permissões concedidas a cada usuário do banco de dados.

---

**16**

Uma equipe alterou o tipo de dado de uma coluna da tabela `Pedido`, de `INT` para `BIGINT`, o que exigiu ajuste em três aplicações que a consomem.

Em relação a esse caso, é correto afirmar que houve

- [ ] (A) plena independência de dados lógica.  
- [ ] (B) plena independência de dados física.  
- [x] (C) limitação da independência de dados lógica, pois a alteração conceitual afetou as aplicações.  
- [ ] (D) violação da independência de dados física, pois alterou-se o armazenamento.  
- [ ] (E) violação da integridade referencial da tabela Pedido.

---

**17**

A independência de dados constitui um dos principais objetivos dos Sistemas Gerenciadores de Banco de Dados, em contraposição aos sistemas baseados em arquivos.

Nos sistemas tradicionais de arquivos, essa independência inexistia porque

- [ ] (A) os dados eram armazenados exclusivamente em memória principal.  
- [x] (B) a descrição da estrutura dos dados estava embutida no código dos programas que os manipulavam. 
- [ ] (C) não havia possibilidade de definir chaves primárias nos arquivos.  
- [ ] (D) todos os programas utilizavam necessariamente o mesmo esquema conceitual.  
- [ ] (E) as consultas eram formuladas exclusivamente em linguagem declarativa.

---

**18**

Uma equipe reorganizou a tabela `Cliente`, aplicando normalização até a Terceira Forma Normal, o que resultou em três tabelas. Para preservar o funcionamento das aplicações existentes, criou-se uma visão com a estrutura original.

Nesse cenário, a visão atua

- [ ] (A) no nível interno, otimizando o acesso físico aos dados.  
- [x] (B) no nível externo, preservando a independência de dados lógica.  
- [ ] (C) no nível conceitual, substituindo o modelo de dados original.  
- [ ] (D) como restrição de integridade referencial entre as três tabelas.  
- [ ] (E) como mecanismo de controle de concorrência entre transações.

---

**19**

A arquitetura de três níveis apresenta finalidades bem delimitadas.

**NÃO** constitui benefício proporcionado por essa arquitetura a

- [ ] (A) possibilidade de alterar o armazenamento sem afetar as aplicações.  
- [ ] (B) apresentação de visões distintas a diferentes grupos de usuários.  
- [ ] (C) separação entre a descrição lógica e a descrição física dos dados.  
- [x] (D) eliminação da necessidade de realizar cópias de segurança do banco.  
- [ ] (E) redução do impacto de alterações estruturais sobre os programas existentes.

---

**20**

Um analista relacionou alterações realizadas em um banco de dados.

**NÃO** é exemplo de alteração amparada pela independência de dados física a

- [ ] (A) criação de um índice sobre uma coluna consultada com frequência.  
- [ ] (B) alteração do método de organização dos arquivos de dados em disco.  
- [ ] (C) migração dos arquivos de dados para outro dispositivo de armazenamento.  
- [x] (D) exclusão de uma coluna utilizada pelas aplicações existentes.  
- [ ] (E) aplicação de compressão sobre os blocos de dados armazenados.