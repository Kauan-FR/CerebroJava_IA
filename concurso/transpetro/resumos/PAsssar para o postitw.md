---
Tipo:
  - resumo
---
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

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 11 — USABILIDADE E NIELSEN      [T-6.1]  │
├─────────────────────────────────────────────────┤
│ usabilidade = atributo | UX = experiência toda  │
│ ISO 9241-11: EFICÁCIA (conseguiu) ·             │
│   EFICIÊNCIA (gastou pouco) · SATISFAÇÃO        │
│   + sempre num CONTEXTO DE USO                  │
│                                                 │
│ 10 heurísticas: status · mundo real · liberdade │
│   consistência · PREVENÇÃO · reconhecer ·       │
│   flexibilidade · minimalista · RECUPERAÇÃO ·   │
│   ajuda                                         │
│ ⚠ 5 previne | 9 trata o erro já ocorrido        │
│ ⚠ 6 novato  | 7 experiente (atalho)             │
│                                                 │
│ HEURÍSTICA = especialista                       │
│ TESTE = usuário real                            │
│ percurso cognitivo = especialista simula novato │
│ regra dos 5 usuários                            │
└─────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────┐
│ CARTÃO 12 — ACESSIBILIDADE             [T-6.1]  │
├─────────────────────────────────────────────────┤
│ usabilidade = fácil | acessibilidade = consegue │
│ inclui limitação temporária e situacional       │
│ desenho universal = p/ todos desde o início     │
│                                                 │
│ WCAG — POUR:                                    │
│   Perceptível ... alt, legenda, contraste       │
│   Operável ...... teclado, tempo                │
│   Compreensível . legível, previsível           │
│   Robusto ....... tecnologia assistiva          │
│ níveis: A → AA (exigido) → AAA                  │
│                                                 │
│ eMAG = governo brasileiro                       │
│ LBI 13.146/2015 = Estatuto da PcD               │
│ ⚠ nunca informar SÓ por cor                     │
└─────────────────────────────────────────────────┘

---

┌─────────────────────────────────────────────────┐
│ CARTÃO 13 — HISTÓRIAS DO USUÁRIO       [T-6.2]  │
├─────────────────────────────────────────────────┤
│ "Como [quem], quero [o quê], para que [porquê]" │
│   → o "para quê" é o VALOR, não pode faltar     │
│                                                 │
│ 3 Cs: Cartão · Conversa · Confirmação           │
│                                                 │
│ INVEST: Independente · Negociável · Valiosa ·   │
│   Estimável · Small (pequena) · Testável        │
│                                                 │
│ critério de aceitação = de UMA história         │
│ definição de pronto   = de TODAS                │
│ épico = grande demais, quebra em histórias      │
└─────────────────────────────────────────────────┘


---


┌─────────────────────────────────────────────────┐
│ CARTÃO 14 — MVP                        [T-6.8]  │
├─────────────────────────────────────────────────┤
│ MVP = menor escopo que VAI AO USUÁRIO REAL,     │
│   entrega valor e gera aprendizado              │
│ ⚠ VIÁVEL = funciona de verdade                  │
│   (não é versão pela metade)                    │
│ ciclo: construir → medir → aprender             │
│                                                 │
│ PROTÓTIPO simula (valida a interface)           │
│ MVP entrega (valida a hipótese de negócio)      │
│                                                 │
│ concierge = manual, usuário SABE                │
│ mágico de Oz = manual, usuário NÃO SABE         │
│ landing page = mede interesse                   │
└─────────────────────────────────────────────────┘