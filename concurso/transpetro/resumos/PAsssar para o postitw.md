---
Tipo:
  - resumo
---
---


┌─────────────────────────────────────────────────┐
│ CARTÃO 18 — PERSONAS                  [T-6.11]  │
├─────────────────────────────────────────────────┤
│ persona = personagem fictício que representa    │
│   um grupo REAL, criado a partir de PESQUISA    │
│ ⚠ não é suposição da equipe                     │
│                                                 │
│ PÚBLICO-ALVO = recorte amplo e estatístico      │
│ PERSONA = um personagem detalhado, com nome,    │
│   contexto, DORES e OBJETIVOS                   │
│                                                 │
│ ATOR (UML) = papel abstrato, o que o sistema    │
│   faz para ele                                  │
│ PERSONA = pessoa, quem ele é                    │
│                                                 │
│ antipersona = quem NÃO é o alvo                 │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 19 — INTERAÇÃO WEB              [T-6.3]  │
├─────────────────────────────────────────────────┤
│ IxD = como o usuário FAZ a tarefa               │
│ AI  = como o usuário ACHA o conteúdo            │
│   AI: organização · rotulagem · navegação ·     │
│       busca                                     │
│                                                 │
│ IxD: ações · FEEDBACK · estados · fluxo         │
│                                                 │
│ affordance = sugere como usar                   │
│ significante = o sinal da affordance            │
│ modelo mental = o que o usuário acredita        │
│ restrição = limita p/ evitar erro               │
│                                                 │
│ RESPONSIVO = 1 layout fluido                    │
│ ADAPTATIVO = layouts distintos por faixa        │
│ mobile first = menor tela primeiro              │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 20 — INTEROPERABILIDADE         [T-6.7]  │
├─────────────────────────────────────────────────┤
│ funcionar igual em navegadores diferentes       │
│ causa: cada um tem seu motor de renderização    │
│                                                 │
│ solução = PADRÕES WEB (W3C, ECMA)               │
│ ⚠ não é uma versão por navegador                │
│                                                 │
│ DEGRADAÇÃO GRACIOSA = do moderno pro antigo     │
│ MELHORIA PROGRESSIVA = da base pro avançado     │
│ polyfill = adiciona recurso que falta           │
│ cross-browser = testar em cada um               │
│                                                 │
│ WCAG: princípio ROBUSTO                         │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 21 — STORYTELLING COM DADOS     [T-6.5]  │
├─────────────────────────────────────────────────┤
│ narrativa que leva à DECISÃO                    │
│ tripé: DADOS · NARRATIVA · VISUAL               │
│ estrutura: contexto → conflito → resolução      │
│                                                 │
│ princípios: conhecer o público · gráfico certo ·│
│   eliminar o excesso · dirigir a atenção ·      │
│   título com a mensagem                         │
│ ⚠ 3D distorce | pizza só poucas fatias          │
│                                                 │
│ tempo → LINHA                                   │
│ categorias → BARRA                              │
│ parte do todo → PIZZA                           │
│ duas variáveis → DISPERSÃO                      │
│ distribuição → HISTOGRAMA                       │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 23 — DADO → INTELIGÊNCIA        [T-7.1]  │
├─────────────────────────────────────────────────┤
│ DADO = bruto, sem contexto                      │
│ INFORMAÇÃO = dado + CONTEXTO                    │
│ CONHECIMENTO = informação INTERPRETADA          │
│ INTELIGÊNCIA = conhecimento aplicado à AÇÃO     │
│                                                 │
│ dado→info: contexto                             │
│ info→conhec: interpretação                      │
│ conhec→intel: decisão                           │
│                                                 │
│ TÁCITO = na cabeça (calado)                     │
│ EXPLÍCITO = documentado (escrito)               │
└─────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────┐
│ CARTÃO 25 — MINERAÇÃO E KPI            [T-7.2]  │
├─────────────────────────────────────────────────┤
│ ASSOCIAÇÃO = itens que coocorrem (cesta)        │
│ CLASSIFICAÇÃO = categoria já conhecida (superv.)│
│ AGRUPAMENTO = grupos por semelhança (não sup.)  │
│ REGRESSÃO = prevê número                        │
│ ANOMALIA = fora do padrão                       │
│ ⚠ "comprados juntos" = associação, sempre       │
│ ⚠ classificação = categoria | regressão = número│
│                                                 │
│ MÉTRICA = valor medido                          │
│ KPI = métrica + OBJETIVO + META                 │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 26 — TIPOS DE DADOS             [T-7.4]  │
├─────────────────────────────────────────────────┤
│ ESTRUTURADO = linhas e colunas, esquema rígido  │
│ SEMIESTRUTURADO = tem MARCADOR, sem esquema fixo│
│   → JSON, XML, HTML, log                        │
│ NÃO ESTRUTURADO = sem organização nenhuma       │
│   → texto livre, imagem, áudio, vídeo           │
│   → exige PLN e IA; é a MAIORIA do dado         │
│                                                 │
│ ⚠ JSON e XML = SEMI, não "não estruturado"      │
│                                                 │
│ DW = tratado, schema-on-WRITE                   │
│ DATA LAKE = bruto, schema-on-READ               │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 27 — OLAP                       [T-7.5]  │
├─────────────────────────────────────────────────┤
│ cubo: fato · medida · dimensão · HIERARQUIA     │
│                                                 │
│ OLTP = Transação, escrita, normalizado, atual   │
│ OLAP = Análise, leitura, dimensional, histórico │
│                                                 │
│ DRILL-DOWN desce (detalha)                      │
│ ROLL-UP sobe (consolida)                        │
│ SLICE = uma dimensão                            │
│ DICE = várias dimensões                         │
│ PIVOT = gira o cubo                             │
│ DRILL-ACROSS = outro fato                       │
│ DRILL-THROUGH = dado de origem                  │
│                                                 │
│ ROLAP = Relacional (escala, lento)              │
│ MOLAP = cubo (rápido, limitado)                 │
│ HOLAP = híbrido                                 │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 28 — DATA WAREHOUSE             [T-7.6]  │
├─────────────────────────────────────────────────┤
│ INMON — 4 características (O-I-N-V):            │
│   Orientado a assunto · Integrado ·             │
│   NÃO VOLÁTIL · Variante no tempo               │
│ ⚠ não volátil = sem UPDATE nem DELETE           │
│                                                 │
│ DW = organização inteira                        │
│ DATA MART = um departamento (recorte do DW)     │
│                                                 │
│ INMON = top-down (DW → marts)                   │
│ KIMBALL = bottom-up (marts → DW)                │
│                                                 │
│ staging = limpeza temporária antes da carga     │
│ ODS = atual e volátil | DW = histórico          │
│                                                 │
│ DW: tratado, schema-on-WRITE, ETL               │
│ LAKE: bruto, schema-on-READ, ELT                │
│   sem governança = data swamp                   │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 29 — MODELAGEM DIMENSIONAL      [T-7.7]  │
├─────────────────────────────────────────────────┤
│ FATO = medidas + FKs (muitas linhas)            │
│ DIMENSÃO = atributos descritivos                │
│ GRANULARIDADE = nível de detalhe do fato        │
│                                                 │
│ ESTRELA = desnormalizada, poucos joins, RÁPIDA  │
│ FLOCO = normalizada, muitos joins, lenta        │
│ CONSTELAÇÃO = vários fatos, dim. conformadas    │
│                                                 │
│ aditiva = soma em tudo                          │
│ SEMIaditiva = soma em algumas, NÃO no tempo     │
│ não aditiva = percentual, média                 │
│                                                 │
│ degenerada = fica no fato (nº cupom)            │
│ PAPEL = várias vezes no MESMO fato              │
│ CONFORMADA = em fatos DIFERENTES                │
│ lixo = flags de baixa cardinalidade juntas      │
│                                                 │
│ SCD 1 sobrescreve | SCD 2 cria linha            │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 30 — FONTES DE DADOS            [T-7.3]  │
├─────────────────────────────────────────────────┤
│ mapear = de onde vem cada dado (antes do ETL)   │
│ documentar: origem · responsável · formato ·    │
│   FREQUÊNCIA · volume · qualidade               │
│                                                 │
│ LINHAGEM = caminho da origem até o relatório    │
│ METADADO = dado sobre o dado                    │
│                                                 │
│ qualidade: completude · acurácia ·              │
│   consistência · atualidade · unicidade         │
│ fonte única de verdade = quem é o DONO do dado  │
│ ⚠ garbage in, garbage out                       │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 31 — PLANILHAS                  [T-7.9]  │
├─────────────────────────────────────────────────┤
│ A1 relativa | $A$1 absoluta                     │
│ $A1 trava coluna | A$1 trava linha               │
│ ⚠ o $ trava o que vem depois                    │
│                                                 │
│ PROCV: 1ª coluna, retorna à DIREITA             │
│   último argumento FALSO/0 = exato              │
│ ⚠ PROCV não busca à ESQUERDA                    │
│   → aí é ÍNDICE + CORRESP                       │
│                                                 │
│ CONT.SE conta | SOMASE soma | ...SES = vários   │
│ ⚠ SOMASE: soma por ÚLTIMO                       │
│   SOMASES: soma por PRIMEIRO                    │
│                                                 │
│ tabela dinâmica = resume sem alterar a origem   │
│ FILTRO oculta | CLASSIFICAÇÃO reordena          │
│                                                 │
│ #N/D não achou · #REF! célula excluída          │
│ #VALOR! tipo errado · #NOME? função errada      │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 32 — INSIGHTS                  [T-7.10]  │
├─────────────────────────────────────────────────┤
│ INSIGHT = descoberta relevante e ACIONÁVEL      │
│ informação DESCREVE | insight EXPLICA e AGE     │
│                                                 │
│ 3 critérios: relevante · ACIONÁVEL · novo       │
│                                                 │
│ caminho: observar → questionar → investigar →   │
│   concluir → agir                               │
│ (descritiva → diagnóstica)                      │
│                                                 │
│ procurar: tendência · sazonalidade · outlier ·  │
│   correlação · concentração (Pareto)            │
│                                                 │
│ ⚠⚠ CORRELAÇÃO ≠ CAUSALIDADE                     │
│ viés de confirmação = só ver o que confirma     │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 33 — CRIPTOGRAFIA               [T-9.19] │
├─────────────────────────────────────────────────┤
│ SIMÉTRICA: 1 chave, RÁPIDA, AES/DES/3DES        │
│   problema = distribuir a chave                 │
│ ASSIMÉTRICA: par, LENTA, RSA/ECC/Diffie-Hellman │
│ HÍBRIDA = assimétrica troca, simétrica cifra    │
│                                                 │
│ ⚠⚠ QUAL CHAVE:                                  │
│   esconder → PÚBLICA DO DESTINATÁRIO            │
│   assinar  → PRIVADA DO REMETENTE               │
│                                                 │
│ confidencialidade = criptografia                │
│ integridade = HASH                              │
│ autenticidade e NÃO REPÚDIO = ASSINATURA        │
└─────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────┐
│ CARTÃO 34 — HASH, ASSINATURA E CERT.   [T-9.19] │
├─────────────────────────────────────────────────┤
│ HASH: unidirecional, tamanho fixo,              │
│   efeito avalanche, resistente a colisão        │
│   seguros: SHA-256, SHA-3                       │
│   quebrados: MD5, SHA-1                         │
│ ⚠ hash não se decifra                           │
│                                                 │
│ ASSINATURA: cifra o HASH com a PRIVADA          │
│   dá integridade + autenticidade + não repúdio  │
│   NÃO dá confidencialidade                      │
│ ⚠ digital ≠ digitalizada (imagem escaneada)     │
│                                                 │
│ CERTIFICADO: liga chave pública a identidade    │
│   padrão X.509                                  │
│   AC EMITE | AR IDENTIFICA | LCR = revogados    │
│   Brasil: ICP-Brasil, AC-Raiz = ITI             │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 35 — ATAQUES I                   [T-9.4] │
├─────────────────────────────────────────────────┤
│ DoS = 1 origem | DDoS = botnet (zumbis)         │
│   atinge DISPONIBILIDADE                        │
│                                                 │
│ SQLi = altera a ESTRUTURA da consulta           │
│   ⚠ defesa = CONSULTA PARAMETRIZADA             │
│                                                 │
│ XSS = script no navegador de OUTRO usuário      │
│   refletido = no link, não fica                 │
│   armazenado = no servidor, atinge todos        │
│   defesa = output encoding, CSP, HttpOnly       │
│                                                 │
│ PATH TRAVERSAL = ../ sai do diretório           │
└─────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────┐
│ CARTÃO 36 — XSS × CSRF                  [T-9.4] │
├─────────────────────────────────────────────────┤
│ XSS  → INJETA código (script no navegador)      │
│ CSRF → FORÇA ação (requisição em nome da vítima)│
│                                                 │
│ XSS explora a confiança do USUÁRIO no site      │
│ CSRF explora a confiança do SITE no usuário     │
│   autenticado (precisa de sessão ativa)         │
│                                                 │
│ defesa XSS  = encoding de saída, CSP            │
│ defesa CSRF = TOKEN anti-CSRF, SameSite         │
│                                                 │
│ zero-day = falha sem correção                   │
│ phishing = engenharia social                    │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 37 — MALWARE                     [T-9.3] │
├─────────────────────────────────────────────────┤
│ VÍRUS = precisa de hospedeiro E de ação do      │
│   usuário (pega carona)                         │
│ WORM = autônomo, autopropaga pela rede          │
│                                                 │
│ ransomware = cifra e cobra → defesa é BACKUP    │
│ spyware = espiona | keylogger = teclas          │
│ rootkit = privilégio + ESCONDE (kernel)         │
│ trojan = disfarça, NÃO replica                  │
│ backdoor = porta p/ acesso futuro               │
│ bot/zumbi → botnet                              │
│                                                 │
│ ⚠ rootkit ESCONDE | backdoor ABRE               │
│                                                 │
│ exploit = código que explora a falha            │
│ zero-day = falha sem correção                   │
│ vulnerabilidade(fraqueza) · ameaça(agente) ·    │
│   risco(probabilidade × impacto)                │
└─────────────────────────────────────────────────┘