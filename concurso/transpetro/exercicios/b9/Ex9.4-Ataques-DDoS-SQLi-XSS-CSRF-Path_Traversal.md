---
Data: 2026-10-15
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Um ataque em que o agente malicioso envia volume massivo de requisições a partir de múltiplas origens comprometidas, esgotando os recursos do servidor e impedindo o atendimento aos usuários legítimos, é denominado

- [x] (A) DDoS.
- [ ] (B) SQL injection.
- [ ] (C) XSS refletido.
- [ ] (D) CSRF.
- [ ] (E) path traversal.

---

**2**

A principal diferença entre um ataque DoS e um ataque DDoS é que o DDoS

- [x] (A) parte de múltiplas origens distribuídas, usualmente máquinas comprometidas que compõem uma botnet.
- [ ] (B) explora vulnerabilidades no código-fonte da aplicação.
- [ ] (C) tem por objetivo a exfiltração de dados sigilosos.
- [ ] (D) depende necessariamente da obtenção prévia de credenciais válidas.
- [ ] (E) ocorre exclusivamente em aplicações web.

---

**3**

Um atacante inseriu, em um campo de formulário, a expressão `' OR '1'='1`, obtendo acesso a registros que não lhe eram destinados.

Esse ataque é denominado

- [ ] (A) cross-site scripting.
- [x] (B) SQL injection.
- [ ] (C) path traversal.
- [ ] (D) negação de serviço.
- [ ] (E) sequestro de sessão por força bruta.

---

**4**

A principal medida de prevenção contra ataques de SQL injection é

- [x] (A) a utilização de consultas parametrizadas (*prepared statements*) com vinculação de parâmetros.
- [ ] (B) o aumento do tempo de expiração das sessões de usuário.
- [ ] (C) a compressão das respostas enviadas pelo servidor.
- [ ] (D) a adoção de certificado digital emitido por autoridade credenciada.
- [ ] (E) a replicação do banco de dados em servidor secundário.

---

**5**

Um atacante conseguiu inserir código de script em um campo de comentário de um site. Esse código passou a ser executado no navegador de todos os visitantes que acessavam a página.

Esse ataque é denominado

- [ ] (A) SQL injection.
- [x] (B) cross-site scripting (XSS) armazenado.
- [ ] (C) cross-site request forgery.
- [ ] (D) path traversal.
- [ ] (E) ataque de força bruta.

---

**6**

Um atacante enviou à vítima um link contendo código malicioso no parâmetro da URL, que é devolvido pelo servidor e executado no navegador no momento da resposta, sem ser armazenado na aplicação.

Esse ataque é denominado XSS

- [ ] (A) armazenado.
- [x] (B) refletido.
- [ ] (C) baseado em DOM exclusivamente.
- [ ] (D) persistente de segundo nível.
- [ ] (E) encadeado por sessão.

---

**7**

Constituem medidas de prevenção contra ataques de cross-site scripting

- [x] (A) a codificação da saída (*output encoding*) e a validação da entrada fornecida pelo usuário.
- [ ] (B) o aumento da capacidade de processamento do servidor web.
- [ ] (C) a desativação dos índices do banco de dados.
- [ ] (D) a replicação assíncrona entre os nós da aplicação.
- [ ] (E) a adoção de chaves simétricas de maior comprimento.

---

**8**

Um usuário autenticado em um sistema bancário acessou, em outra aba, uma página maliciosa que submeteu automaticamente uma requisição de transferência ao banco, aproveitando-se da sessão ativa do usuário.

Esse ataque é denominado

- [x] (A) cross-site request forgery (CSRF).
- [ ] (B) cross-site scripting armazenado.
- [ ] (C) SQL injection cega.
- [ ] (D) negação de serviço distribuída.
- [ ] (E) path traversal.

---

**9**

A principal medida de prevenção contra ataques de CSRF é

- [x] (A) a utilização de token antifalsificação, único por sessão ou requisição, validado pelo servidor.
- [ ] (B) a codificação da saída apresentada ao navegador.
- [ ] (C) o uso de consultas parametrizadas no acesso ao banco de dados.
- [ ] (D) a limitação do tamanho dos arquivos enviados pelo usuário.
- [ ] (E) a desativação do protocolo HTTPS nas requisições internas.

---

**10**

Uma diferença entre XSS e CSRF é que o XSS

- [x] (A) executa código malicioso no navegador da vítima, enquanto o CSRF induz o navegador da vítima a enviar requisição legítima não autorizada pelo usuário.
- [ ] (B) induz o envio de requisições não autorizadas, enquanto o CSRF executa scripts no navegador.
- [ ] (C) explora falhas no banco de dados, enquanto o CSRF explora falhas no sistema operacional.
- [ ] (D) exige autenticação prévia da vítima, enquanto o CSRF dispensa sessão ativa.
- [ ] (E) ocorre apenas em aplicações desktop, enquanto o CSRF ocorre em aplicações web.

---

**11**

Um atacante manipulou o parâmetro de nome de arquivo em uma requisição, informando a sequência `../../etc/passwd`, e obteve acesso a arquivo situado fora do diretório previsto pela aplicação.

Esse ataque é denominado

- [x] (A) path traversal (travessia de diretório).
- [ ] (B) SQL injection.
- [ ] (C) cross-site scripting.
- [ ] (D) negação de serviço.
- [ ] (E) escalonamento de privilégio por sessão.

---

**12**

A prevenção contra ataques de path traversal apoia-se principalmente

- [x] (A) na validação e na normalização dos caminhos informados, restringindo o acesso a um diretório previamente autorizado.
- [ ] (B) no aumento do número de réplicas do servidor de aplicação.
- [ ] (C) na adoção de algoritmos de resumo criptográfico mais robustos.
- [ ] (D) na redução do tempo de expiração dos certificados digitais.
- [ ] (E) na desativação do registro de logs de acesso.

---

**13**

Um conjunto de computadores infectados e controlados remotamente por um atacante, utilizado para desferir ataques coordenados, é denominado

- [x] (A) botnet.
- [ ] (B) honeypot.
- [ ] (C) sandbox.
- [ ] (D) bastion host.
- [ ] (E) cluster de alta disponibilidade.

---

**14**

Uma organização implantou solução capaz de inspecionar o tráfego HTTP, identificando e bloqueando requisições que caracterizem tentativas de SQL injection e de XSS antes que alcancem a aplicação.

Essa solução é denominada

- [x] (A) WAF (*web application firewall*).
- [ ] (B) SIEM.
- [ ] (C) DLP.
- [ ] (D) VPN de acesso remoto.
- [ ] (E) servidor de autenticação SSO.

---

**15**

Um atacante interceptou a comunicação entre o usuário e o servidor, passando a ler e eventualmente alterar as mensagens trocadas sem que as partes percebessem.

Esse ataque é denominado

<font color="#00b050">- [ ] (A) *man-in-the-middle*.</font>
<font color="#ff0000">- [x] (B) *buffer overflow*.</font>
- [ ] (C) *phishing* direcionado.
- [ ] (D) *privilege escalation*.
- [ ] (E) *session fixation* por token estático.

>[!fail] man-in-the-middle x buffer overflow
>||Onde age|Como funciona|
|---|---|---|
|**MITM**|**no caminho** entre as partes|o atacante se posiciona entre cliente e servidor e retransmite o tráfego, lendo ou alterando|
|**Buffer overflow**|**na memória** do processo|grava mais dados que o buffer comporta, sobrescrevendo >áreas adjacentes para desviar a execução|

---

**16**

Os ataques a aplicações web apresentam características bem delimitadas.

**NÃO** constitui característica do ataque de SQL injection a

- [ ] (A) exploração da ausência de tratamento adequado da entrada fornecida pelo usuário.
- [ ] (B) possibilidade de leitura, alteração ou exclusão de dados não autorizados.
- [x] (C) execução de código no navegador dos demais usuários da aplicação.
- [ ] (D) possibilidade de contornar mecanismos de autenticação da aplicação.
- [ ] (E) prevenção por meio do uso de consultas parametrizadas.