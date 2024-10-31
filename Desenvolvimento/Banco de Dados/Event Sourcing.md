---
tags:
  - Database
---

[[CQRS - Banco de Dados]]

O CQRS também lida com Event Sourcing, que é basicamente a fonte de qualquer evento ou ação tomada no sistema. Com esse histórico você pode consultar quaisquer mudanças que fizeram nele. Por exemplo: se houve a alteração de um nome, você consegue verificar quando isso aconteceu e o que foi alterado.

Isso é muito vantajoso, principalmente quando você trabalha em sistemas que precisam de uma grande auditoria e seguir diversas regras de compliance.

Pensando nesses aspectos você pode implementar o CQRS no seu dia a dia, mas não se esqueça de considerar as situações nas quais isso vai ser realmente necessário e vantajoso para o seu trabalho.