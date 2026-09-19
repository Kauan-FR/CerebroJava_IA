---
Data: 2026-09-19
tags:
  - transpetro
  - exercicio
Tipo:
  - exercicio
---
---

**1**

No paradigma estruturado, a técnica que representa graficamente o fluxo de dados entre processos, entidades externas e depósitos de dados é o

- [x] (A) Diagrama de Fluxo de Dados (DFD).  
- [ ] (B) Diagrama de Classes.  
- [ ] (C) Diagrama de Sequência.  
- [ ] (D) Modelo Entidade-Relacionamento.  
- [ ] (E) Diagrama de Casos de Uso.

---

**2**

No projeto estruturado, o grau de dependência entre os módulos de um sistema é denominado

- [ ] (A) coesão.  
- [x] (B) acoplamento.  
- [ ] (C) cardinalidade.  
- [ ] (D) granularidade.  
- [ ] (E) modularidade.

---

**3**

Considera-se desejável, no projeto de software, que os módulos apresentem

<font color="#00b050">- [ ] (A) alta coesão e baixo acoplamento.  </font>
<font color="#ff0000">- [x] (B) baixa coesão e alto acoplamento.  </font>
- [ ] (C) alta coesão e alto acoplamento.  
- [ ] (D) baixa coesão e baixo acoplamento.  
- [ ] (E) coesão e acoplamento equivalentes entre si.

>[!fail] alta coesão e baixo acoplamento
>**Coesão** — o quanto as responsabilidades **dentro** de um módulo pertencem uma à outra. Alta coesão significa que a classe faz uma coisa só e faz bem. É o Single Responsibility do SOLID.
>**Acoplamento** — o quanto um módulo **depende** de outro. Baixo acoplamento significa que mudar uma classe não obriga a mudar as outras. É o que injeção de dependência e programação por interface buscam.

---

**4**

No paradigma orientado a objetos, o mecanismo que oculta os detalhes internos de implementação, expondo apenas uma interface controlada de acesso, é denominado

- [ ] (A) herança.  
- [ ] (B) polimorfismo.  
- [x] (C) encapsulamento.  
- [ ] (D) instanciação.  
- [ ] (E) agregação.

---

**5**

Uma classe `Gerente` foi definida a partir da classe `Funcionario`, reaproveitando seus atributos e métodos e acrescentando comportamentos específicos.

Esse mecanismo é denominado

- [x] (A) herança.  
- [ ] (B) encapsulamento.  
- [ ] (C) sobrecarga.  
- [ ] (D) composição.  
- [ ] (E) instanciação.

---

**6**

Um desenvolvedor criou, na mesma classe, três métodos com o mesmo nome, diferenciados pela quantidade e pelo tipo de seus parâmetros.

Esse recurso é denominado

- [ ] (A) sobrescrita (_override_).  
- [x] (B) sobrecarga (_overload_).  
- [ ] (C) herança múltipla.  
- [ ] (D) encapsulamento.  
- [ ] (E) delegação.

---

**7**

Uma subclasse redefiniu, com implementação própria, um método já existente na superclasse, mantendo a mesma assinatura.

Esse recurso é denominado

- [ ] (A) sobrecarga (_overload_).  
- [x] (B) sobrescrita (_override_).  
- [ ] (C) agregação.  
- [ ] (D) abstração.  
- [ ] (E) instanciação.

---

**8**

A capacidade de objetos de classes distintas responderem de formas diferentes à mesma mensagem é denominada

- [x] (A) polimorfismo.  
- [ ] (B) encapsulamento.  
- [ ] (C) herança.  
- [ ] (D) coesão.  
- [ ] (E) persistência.

---

**9**

No paradigma orientado a objetos, a relação entre classe e objeto corresponde à relação entre

- [ ] (A) instância e modelo, respectivamente.  
- [x] (B) modelo e instância, respectivamente.  
- [ ] (C) método e atributo, respectivamente.  
- [ ] (D) interface e implementação, respectivamente.  
- [ ] (E) superclasse e subclasse, respectivamente.

---

**10**

Uma classe `Pedido` é composta por objetos da classe `ItemPedido`, de modo que os itens não existem independentemente do pedido a que pertencem.

Esse tipo de relacionamento é denominado

- [x] (A) composição.  
- [ ] (B) agregação.  
- [ ] (C) herança.  
- [ ] (D) dependência.  
- [ ] (E) realização.

---

**11**

Na UML, o diagrama que representa as classes do sistema, seus atributos, operações e os relacionamentos entre elas é o diagrama de

- [x] (A) classes.  
- [ ] (B) sequência.  
- [ ] (C) atividades.  
- [ ] (D) estados.  
- [ ] (E) implantação.

---

**12**

Na UML, o diagrama que representa a troca de mensagens entre objetos ao longo do tempo, evidenciando a ordem temporal das interações, é o diagrama de

- [ ] (A) classes.  
- [ ] (B) componentes.  
- [x] (C) sequência.  
- [ ] (D) pacotes.  
- [ ] (E) objetos.

---

**13**

Na UML, classificam-se como diagramas comportamentais os diagramas de

- [ ] (A) classes, componentes e implantação.  
- [x] (B) casos de uso, sequência e atividades.  
- [ ] (C) objetos, pacotes e estrutura composta.  
- [ ] (D) implantação, perfil e componentes.  
- [ ] (E) classes, objetos e pacotes.

---

**14**

Em um diagrama de casos de uso, o caso de uso "Emitir Nota Fiscal" executa obrigatoriamente, como parte de seu fluxo, o caso de uso "Calcular Impostos".

O relacionamento adequado entre eles é

- [x] (A) _include_.  
- [ ] (B) _extend_.  
- [ ] (C) generalização.  
- [ ] (D) associação simples.  
- [ ] (E) realização.

---

**15**

Em um diagrama de casos de uso, o caso de uso "Aplicar Desconto Promocional" ocorre apenas em determinadas condições, de forma opcional, acrescentando comportamento ao caso de uso "Registrar Venda".

O relacionamento adequado entre eles é

- [ ] (A) _include_.  
- [x] (B) _extend_.  
- [ ] (C) composição.  
- [ ] (D) agregação.  
- [ ] (E) dependência de instalação.

---

**16**

Uma diferença entre o paradigma estruturado e o paradigma orientado a objetos é que o estruturado

- [x] (A) organiza o sistema em torno de funções e do fluxo de dados, enquanto o orientado a objetos o organiza em torno de objetos que reúnem dados e comportamento.  
- [ ] (B) organiza o sistema em torno de objetos, enquanto o orientado a objetos o organiza em torno de funções.  
- [ ] (C) dispensa a modelagem de dados, enquanto o orientado a objetos a exige.  
- [ ] (D) aplica-se exclusivamente a sistemas web, enquanto o orientado a objetos se aplica a sistemas legados.  
- [ ] (E) impede a decomposição do sistema em módulos, enquanto o orientado a objetos a permite.

---

**17**

A análise e o projeto estruturados apresentam técnicas próprias.

**NÃO** constitui técnica do paradigma estruturado o

- [ ] (A) Diagrama de Fluxo de Dados.  
- [ ] (B) dicionário de dados.  
<font color="#00b050">- [ ] (C) diagrama de sequência da UML.  </font>
- [ ] (D) diagrama de estrutura modular.  
<font color="#ff0000">- [x] (E) uso de português estruturado para especificação de processos.</font>

>[!fail] UML
>UML é notação do paradigma **orientado a objetos**. Não pertence ao estruturado em nenhuma versão.

---

**18**

Um analista relacionou conceitos atribuídos ao paradigma orientado a objetos.

**NÃO** constitui conceito desse paradigma a

- [ ] (A) herança entre classes.  
- [ ] (B) encapsulamento dos atributos.  
- [ ] (C) polimorfismo de métodos.  
- [x] (D) decomposição funcional descendente em sub-rotinas.  
- [ ] (E) abstração de entidades do domínio em classes.