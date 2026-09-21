---
Tipo:
  - resumo
---
---

┌─────────────────────────────────────────────────┐
│ CARTÃO 7 — ESTRUTURADO × OO / UML      [T-5.3]  │
├─────────────────────────────────────────────────┤
│ estruturado = FUNÇÃO, separa dado de processo   │
│ OO = OBJETO, junta dado + comportamento         │
│                                                 │
│ DFD — 4 elementos: processo · fluxo ·           │
│   depósito · entidade externa                   │
│ contexto = DFD nível 0 (1 só processo)          │
│ ⚠ DFD = função | DER = dados                    │
│                                                 │
│ UML estruturais (foto): classes · objetos ·     │
│   componentes · implantação · pacotes ·         │
│   estrutura composta · perfil                   │
│ UML comportamentais (filme): casos de uso ·     │
│   atividade · máq. de estados · sequência ·     │
│   comunicação · tempo · visão geral             │
│                                                 │
│ SEQUÊNCIA = tempo | COMUNICAÇÃO = conexão       │
│ «include» = SEMPRE | «extend» = ÀS VEZES        │
│ agregação = losango VAZIO (parte sobrevive)     │
│ composição = losango CHEIO (parte morre)        │
│                                                 │
│ upper CASE = início | lower CASE = fim          │
│ FORWARD = modelo→código | REVERSE = código→mod. │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 8 — V&V, ERRO E NÍVEIS          [T-5.4]  │
├─────────────────────────────────────────────────┤
│ VERIFICAÇÃO = jeito certo (vs especificação)    │
│ VALIDAÇÃO   = software certo (vs necessidade)   │
│ ⚠ verificação não é só estática                 │
│                                                 │
│ erro = PESSOA | defeito = CÓDIGO                │
│ falha = EXECUÇÃO                                │
│                                                 │
│ Níveis: unidade → integração → sistema →        │
│         aceitação (usuário)                     │
│ integração = comunicação ENTRE módulos          │
│ STUB = simula o chamado (top-down)              │
│ DRIVER = simula quem chama (bottom-up)          │
│ alfa = casa do dev | beta = casa do cliente     │
└─────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────┐
│ CARTÃO 9 — TÉCNICAS E PRINCÍPIOS       [T-5.4]  │
├─────────────────────────────────────────────────┤
│ BRANCA = vê o código (caminhos, cobertura,      │
│   complexidade ciclomática) — unidade           │
│ PRETA = só entrada→saída (particionamento de    │
│   equivalência, VALOR-LIMITE) — sistema         │
│                                                 │
│ regressão = não quebrou o que funcionava        │
│   → principal alvo de automação                 │
│ CARGA = esperado | ESTRESSE = além do limite    │
│ smoke = a build está estável?                   │
│                                                 │
│ Princípios: presença nunca ausência · exaustivo │
│   impossível · antecipado é mais barato ·       │
│   agrupamento (Pareto) · paradoxo do pesticida ·│
│   contexto · ausência de erros é ilusão         │
│                                                 │
│ TDD: teste antes. RED → GREEN → REFACTOR        │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 10 — AMBIENTES E FERRAMENTAS    [T-5.5]  │
├─────────────────────────────────────────────────┤
│ dev → teste → HOMOLOGAÇÃO → produção            │
│ homologação = usuário aprova, espelha produção  │
│                                                 │
│ Git = distribuído | SVN = centralizado          │
│ commit = LOCAL | push = REMOTO                  │
│ fetch = só baixa | pull = fetch + merge         │
│ merge preserva | rebase lineariza               │
│                                                 │
│ CI = commit dispara build + teste               │
│ DELIVERY = pronto, liberação manual             │
│ DEPLOYMENT = vai sozinho pra produção           │
│ DevOps = cultura dev + ops                      │
│                                                 │
│ container = compartilha kernel, leve            │
│ VM = SO completo, hypervisor                    │
└─────────────────────────────────────────────────┘