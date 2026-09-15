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

ITIL × COBIT

ITIL  COMO operar serviços
COBIT O QUE governar na TI

ITIL 4: SVS + cadeia de valor + práticas
 ⚠ 5 fases = v3 (antigo)
 incidente = rápido / problema = causa raiz

COBIT 5 domínios
 EDM  governança (avaliar/dirigir/monitorar)
 APO  planejar
 BAI  construir
 DSS  operar/suportar
 MEA  medir/auditar
 ⚠ só EDM é governança · sigla MEA

governança = o QUÊ / gestão = o COMO