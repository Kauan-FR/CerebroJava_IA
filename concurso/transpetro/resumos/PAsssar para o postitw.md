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