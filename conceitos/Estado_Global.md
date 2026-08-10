---
Data: 2026-08-10
tags:
  - java
  - conceito
---
## O que é

O estado global é quando uma aplicação ela quando copilada em uma maquina funciona, mas quando copilada em outra não funciona. Isso aconteceu com o `Locale.setDefalt()`, pois assim que determinamos o local que aquele resultado tem que ser mostrado, por conta do local da maquina ser igual ao do sistema, quando o sistema copila ele parece estar correto, mas isso pode se tornar um erro bem sutil.