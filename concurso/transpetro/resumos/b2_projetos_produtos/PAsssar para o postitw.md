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
