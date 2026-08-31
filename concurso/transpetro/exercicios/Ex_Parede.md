---
Data: 2026-08-26
---
---
## 1.1 Modelagem conceitual

1.1 → ?

qual nível depende do SGBD?
normalização é de qual nível?
identificador é decisão de qual nível?

vários telefones = qual atributo?
endereço em partes = qual atributo?
idade a partir de nascimento = qual?

Médico (1,n)—Realiza—(1,1) Consulta
 quantas consultas por médico?
 quantos médicos por consulta?
 o par está colado em quem?

grau = ?
cardinalidade = ?
quero contar colunas → ?
quero contar linhas → ?

independência FÍSICA = ?
independência LÓGICA = ?
criar índice → qual das duas?

existe independência referencial?

---
## 1.2 Criação e alteração dos modelos lógicos e físicos

1.2 → ?

1:1 obrigatório-obrigatório → ?
1:1 obrigatório-opcional → onde vai a FK?
1:1 opcional-opcional → ?
1:N → onde vai a FK? por quê?
N:M → quantas tabelas? qual a PK?

em 1:1, o que garante que não vira 1:N?

atributo multivalorado vira ?
atributo composto vira ?

herança: quais as 3 estratégias?
"subclasse como multivalorado" existe?

═══ FÍSICO ═══
NOT NULL faz o quê?
UNIQUE faz o quê?
CHECK faz o quê?
DEFAULT faz o quê?
SEQUENCE faz o quê?
ÍNDICE faz o quê?

quero limitar a 2 valores → ?
quero gerar valor sequencial → ?

índice reduz espaço?
índice deixa escrita mais rápida?

índice (A,B): filtra por B sozinho?

ADD COLUMN NOT NULL com dados → precisa de quê?
renomear tabela quebra o quê?

catálogo guarda o quê?
log de transações guarda o quê?
"estruturas criadas" → qual dos dois?

chave natural que muda muito → usar o quê?

---
## 1.3 Modelo relacional

1.3 → ?

"relacional" vem de quê?

relação = ?    tupla = ?
atributo = ?   domínio = ?

esquema = ?
instância = ?
qual dos dois muda a cada INSERT?

superchave = ?
candidata = ?
ordem: super ⊃ ? ⊃ ?
superchave precisa ter 2+ atributos?

integridade de ENTIDADE garante o quê?
integridade REFERENCIAL garante o quê?
enunciado fala de PK → qual?
enunciado fala de FK → qual?

seleção σ filtra o quê?
projeção π filtra o quê?
quero filtrar linhas → ?
quero cortar colunas → ?

junção = ? + ?
INNER descarta o quê?
LEFT preserva o quê?
achar AUSÊNCIA → como?

"todas as X, inclusive as sem Y" → ?
"todas as X, menos as sem Y" → ?
"cursou TODAS as disciplinas" → ?

"uma única lista, sem repetir" → ?
"que estão nas duas" → ?
"ausentes na segunda" → ?

CARTESIANO
 tuplas: soma ou multiplica?
 atributos: soma ou multiplica?

autojunção: e1 é qual nível?
             e2 é qual nível?
 netos → retorna e1 ou e2?

---
## 1.4 Normalização

1.4 → ?

1FN elimina o quê?
2FN elimina o quê?
3FN elimina o quê?
FNBC exige o quê de X em X→Y?

célula com 2 valores → qual FN?
depende de PARTE da chave → qual FN?
não-chave → não-chave → qual FN?
telefone1, telefone2, telefone3 → qual FN?

⚠ CHAVE SIMPLES pode ter
  dependência PARCIAL?

chave simples já está em qual FN?

3FN sem FNBC acontece quando?

em 3FN → está em 2FN?
em 1FN → está em 2FN?
ordem: BCNF ⊂ ? ⊂ ? ⊂ ?

as 3 anomalias?
causa de todas elas?
 não consigo cadastrar → ?
 apaguei e perdi junto → ?
 alterei uma, esqueci outra → ?

CASCADE apagando filho é anomalia?
FK rejeitando insert é anomalia?

normalizar acelera ou desacelera leitura?
quem acelera consulta analítica?

extraí 2 determinantes → quantas relações?

4FN elimina o quê?

---
## 1.5 Integridade referencial

1.5 → ?

FK pode apontar p/ coluna UNIQUE?
por quê? (o que a FK precisa do alvo?)

PK composta por 2 colunas
 → a FK tem quantas colunas?
 2 FKs separadas resolvem?

remover FK impede JOIN?
o que acontece se remover a FK?

FOREIGN KEY age na escrita ou leitura?
JOIN age na escrita ou leitura?

carga de dados: qual tabela primeiro?

ON DELETE SET NULL numa coluna
que é parte da PK — funciona?

═══════════════════
alternativa com "em hipótese alguma"
→ certa ou errada?

---
## 1.6 Metadados

1.6 → ?

metadado é estrutura ou conteúdo?

privilégios de usuário:
 catálogo ou log?
sequência de operações de transação:
 catálogo ou log?

schema-on-write valida quando? quem?
schema-on-read  valida quando? quem?
no NoSQL a estrutura deixa de existir?

"de onde veio e o que mudou" → ?
"estatística do dado real" → ?
"glossário corporativo" → ?
data lake sem catalogação vira ?

---

## 1.7 Modelagem dimensional

1.7 → ?

grão diário permite análise por hora?
por quê?

surrogate key serve pra quê?
SCD 2 funciona sem surrogate key?

ROLAP guarda onde?
MOLAP guarda onde?
qual é mais rápido? qual escala melhor?

DEGENERADA fica onde?
PAPEL: mesmo fato ou fatos diferentes?
CONFORMADA: mesmo fato ou fatos diferentes?
JUNK agrupa o quê?

data mart é o quê?
staging area é o quê?
DW: schema-on-? · lake: schema-on-?

top-down é de quem? bottom-up?

"cubo degenerado" existe?

---

## 1.8 Avaliação de modelos de dados

1.8 → ?

regra de negócio diz "pode" ou "deve"
 → mexe em qual cardinalidade?
regra diz "quantos"
 → qual cardinalidade?

completude verifica o quê?
minimalidade verifica o quê?
legibilidade verifica o quê?
flexibilidade verifica o quê?

verificação confere contra o quê?
validação confere contra o quê?
qual das duas é com o usuário?

tabela com 47 colunas, 30 nulas
 → hipótese?
preco_2024, preco_2025, preco_2026
 → qual critério ferido?
Cliente, Comprador e Consumidor
 juntos → problema de quê?

---

## 1.9_Engenharia_reversa

1.9 → ?

banco → modelo = ?
modelo → banco = ?
corrige e regera = ?
sincroniza nos 2 sentidos = ?

reengenharia tem quantos passos?

banco sem restrições:
 analisar conteúdo pra inferir chave = ?
modelo desatualizado vs produção:
 recurso = ?

engenharia reversa recupera a
INTENÇÃO DE NEGÓCIO da entidade?