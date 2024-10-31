---
tags:
  - Arquitetura
Date: 2024-10-20
---
[[Arquitetura]]
# O que e Arquitetura

arquitetura fala mais sobre como o sistema interage como um todo.
Como os serviços se interligam oque fazem e como fazem a interligação 
Oque precisam para funcionar.

-  **Arquitetura serverless**
solução de aplicativo que depende de serviços de terceiros para gerenciar a complexidade dos servidores e o gerenciamento de back-end.

| _Back-end como serviço (BaaS)_ | _Funções como serviço (FaaS)_ |
| ------------------------------ | ----------------------------- |
O provedor mais famoso de API sem servidor é o Amazon AWS Lambda

-  **Arquitetura orientada a eventos**
desacoplar as partes do sistema e cada parte será acionada quando um evento interessante de outra parte for acionado.
- **Arquitetura de micros-serviços**
Depende do desenvolvimento de serviços modulares pequenos e independentes, em que cada serviço resolve um problema específico ou executa uma tarefa exclusiva e esses módulos se comunicam por meio de uma API bem definida para atender à meta de negócios