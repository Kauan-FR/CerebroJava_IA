---
Tipo:
  - resumo
---
RECURSO CERTO PARA CADA OBJETIVO  [T-1.17]

⚠ antes de marcar, pergunte:
  o enunciado quer...

 VALIDAR valor .......... CHECK
 ACELERAR busca ......... ÍNDICE
 REDUZIR volume lido .... PARTIÇÃO
 evitar join ............ DESNORMALIZAÇÃO
 gerar valor ............ SEQUENCE

═══ ÍNDICE — o que ele NÃO faz ═══
 ⚠ NÃO impede consultar outras colunas
 ⚠ NÃO reduz espaço (ocupa mais)
 ⚠ NÃO elimina coleta de estatística
 só ACELERA a coluna indexada,
 e cobra escrita + espaço + manutenção

═══ CUSTO × BENEFÍCIO DO ÍNDICE ═══
 CUSTO   espaço, escrita lenta,
         manutenção, otimizador
 BENEF.  reduz tempo de consulta
 ⚠ em questão negativa, o benefício
   é o intruso

---

IN-MEMORY / QUALIDADE / LAKE / BIG DATA

in-memory: RAM, rápido
 ⚠ volátil → snapshot + log

QUALIDADE
 completude · precisão · consistência
 unicidade · atualidade · validade

DADOS MESTRES = referência central
 (cliente, produto)
 MDM = fonte única de verdade

LAKE vs DW
 bruto/tratado · on-read/on-write
 ELT / ETL
 lake sem governança = swamp

ETL transforma ANTES
ELT transforma DEPOIS

BIG DATA 5V: Volume Variedade
 Velocidade Veracidade Valor

---

SCRUM / KANBAN

PILARES transparência inspeção adaptação
VALORES compromisso foco abertura
        respeito coragem

PAPÉIS
 PO   o QUÊ + prioridade
 DEVS o COMO
 SM   facilitador (não é chefe)

EVENTOS sprint planning daily
        review retro
 ⚠ review=PRODUTO · retro=PROCESSO

ARTEFATOS product backlog · sprint
          backlog · increment
 DoD = quando está pronto

KANBAN fluxo contínuo · WIP limit

PROJETO tem fim / PRODUTO contínuo

---

SAFe

Scaled Agile Framework
ágil em organização GRANDE

4 níveis:
 Team · Program(ART) · Large Solution
 · Portfolio

ART = Agile Release Train
 5-12 times juntos, ritmo fixo
 (o coração do SAFe)

PI = Program Increment (8-12 semanas)

outros: LeSS, Nexus, Spotify
SAFe = o mais pesado

---

