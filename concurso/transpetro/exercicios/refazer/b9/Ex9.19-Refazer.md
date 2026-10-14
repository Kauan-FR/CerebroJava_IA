---
Data: 2026-10-14
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

Na criptografia simétrica, utiliza-se

- [ ] (A) a mesma chave para cifrar e decifrar a informação.
- [ ] (B) um par de chaves distintas, sendo uma pública e outra privada.
- [ ] (C) exclusivamente funções de resumo criptográfico.
- [ ] (D) uma chave diferente a cada bloco processado, descartada em seguida.
- [ ] (E) apenas a chave pública do destinatário.

---

**2**

Na criptografia assimétrica, a mensagem cifrada com a chave pública do destinatário

- [ ] (A) pode ser decifrada por qualquer detentor da mesma chave pública.
- [ ] (B) somente pode ser decifrada com a chave privada correspondente.
- [ ] (C) somente pode ser decifrada com a chave privada do remetente.
- [ ] (D) dispensa o uso de qualquer chave para ser lida.
- [ ] (E) é convertida automaticamente em resumo criptográfico.

---

**3**

Uma vantagem da criptografia simétrica sobre a assimétrica é

- [ ] (A) o melhor desempenho no processamento de grandes volumes de dados.
- [ ] (B) a dispensa do compartilhamento prévio de chave entre as partes.
- [ ] (C) a garantia intrínseca de não repúdio.
- [ ] (D) a eliminação da necessidade de gestão de chaves.
- [ ] (E) a capacidade de gerar assinaturas digitais sem chave privada.

---

**4**

Constituem exemplos de algoritmos de criptografia simétrica

- [ ] (A) AES e 3DES.
- [ ] (B) RSA e ECC.
- [ ] (C) SHA-256 e MD5.
- [ ] (D) Diffie-Hellman e DSA.
- [ ] (E) bcrypt e scrypt.

---

**5**

Constituem exemplos de algoritmos de criptografia assimétrica

- [ ] (A) AES e ChaCha20.
- [ ] (B) RSA e ECC.
- [ ] (C) SHA-1 e SHA-512.
- [ ] (D) HMAC e CMAC.
- [ ] (E) DES e RC4.

---

**6**

Uma função de resumo criptográfico (*hash*) caracteriza-se por

- [ ] (A) produzir saída de tamanho fixo e ser inviável de reverter computacionalmente.
- [ ] (B) permitir a recuperação do conteúdo original a partir do resumo gerado.
- [ ] (C) produzir saída de tamanho proporcional à entrada processada.
- [ ] (D) exigir uma chave privada para gerar o resumo.
- [ ] (E) gerar resumos distintos a cada execução sobre a mesma entrada.

---

**7**

A propriedade de uma função de resumo segundo a qual é inviável encontrar duas entradas distintas que produzam o mesmo resumo é denominada resistência

- [ ] (A) à colisão.
- [ ] (B) à força bruta.
- [ ] (C) à engenharia reversa de chave.
- [ ] (D) ao desgaste criptográfico.
- [ ] (E) à interceptação em trânsito.

---

**8**

Em um sistema de autenticação, recomenda-se armazenar as senhas dos usuários

- [ ] (A) em texto claro, protegidas por controle de acesso ao banco.
- [ ] (B) cifradas com algoritmo simétrico reversível.
- [ ] (C) como resumo criptográfico gerado com função específica para senhas e valor aleatório adicional (*salt*).
- [ ] (D) codificadas em Base64 antes da gravação.
- [ ] (E) assinadas digitalmente com a chave privada do servidor.

---

**9**

A assinatura digital de um documento é gerada, essencialmente, por meio da cifragem

- [ ] (A) do resumo criptográfico do documento com a chave privada do signatário.
- [ ] (B) do documento integral com a chave pública do destinatário.
- [ ] (C) do resumo criptográfico do documento com a chave pública do signatário.
- [ ] (D) do documento integral com uma chave simétrica compartilhada.
- [ ] (E) da chave privada do signatário com o resumo do documento.

---

**10**

A assinatura digital assegura, principalmente,

- [ ] (A) a confidencialidade do conteúdo transmitido.
- [ ] (B) a autenticidade, a integridade e o não repúdio do documento.
- [ ] (C) a disponibilidade do serviço ao destinatário.
- [ ] (D) a anonimização dos dados pessoais contidos no documento.
- [ ] (E) a compressão do conteúdo antes da transmissão.

---

**11**

Para verificar uma assinatura digital, o destinatário utiliza

- [ ] (A) a chave pública do signatário, comparando o resumo obtido com o resumo calculado sobre o documento recebido.
- [ ] (B) a chave privada do signatário, recalculando o documento integral.
- [ ] (C) sua própria chave privada, decifrando o documento original.
- [ ] (D) uma chave simétrica previamente compartilhada com o signatário.
- [ ] (E) o certificado da autoridade certificadora raiz, sem consultar o documento.

---

**12**

No envelope digital, o conteúdo da mensagem é cifrado com uma chave

- [ ] (A) simétrica, gerada para aquela comunicação, a qual é então cifrada com a chave pública do destinatário.
- [ ] (B) assimétrica pública do destinatário, dispensando qualquer chave simétrica.
- [ ] (C) privada do remetente, decifrada pela chave privada do destinatário.
- [ ] (D) de resumo criptográfico, verificada pela autoridade certificadora.
- [ ] (E) simétrica permanente, compartilhada previamente por canal seguro.

---

**13**

A adoção do envelope digital justifica-se porque ele

- [ ] (A) combina o desempenho da criptografia simétrica com a segurança da distribuição de chaves da assimétrica.
- [ ] (B) dispensa o uso de certificados digitais na comunicação.
- [ ] (C) elimina a necessidade de verificar a integridade da mensagem.
- [ ] (D) substitui a assinatura digital na garantia do não repúdio.
- [ ] (E) reduz o tamanho da mensagem transmitida pela rede.

---

**14**

Um certificado digital tem por finalidade

- [ ] (A) vincular uma chave pública à identidade de seu titular, atestada por uma autoridade certificadora.
- [ ] (B) armazenar a chave privada do titular em repositório público.
- [ ] (C) cifrar o conteúdo das mensagens trocadas entre as partes.
- [ ] (D) gerar resumos criptográficos dos documentos assinados.
- [ ] (E) substituir a necessidade de autenticação dos usuários.

---

**15**

Na Infraestrutura de Chaves Públicas Brasileira (ICP-Brasil), a entidade responsável por verificar presencialmente a identidade do solicitante e encaminhar o pedido de emissão do certificado é a

- [ ] (A) Autoridade Certificadora (AC).
- [ ] (B) Autoridade de Registro (AR).
- [ ] (C) Autoridade Certificadora Raiz.
- [ ] (D) Lista de Certificados Revogados (LCR).
- [ ] (E) Autoridade Nacional de Proteção de Dados.

---

**16**

Os mecanismos criptográficos apresentam finalidades bem delimitadas.

**NÃO** constitui finalidade da assinatura digital a

- [ ] (A) comprovação da autoria do documento assinado.
- [ ] (B) detecção de alterações no conteúdo após a assinatura.
- [ ] (C) impossibilidade de o signatário negar a autoria posteriormente.
- [ ] (D) garantia de que o conteúdo do documento permanecerá sigiloso durante a transmissão.
- [ ] (E) vinculação da assinatura a um par de chaves associado ao signatário.