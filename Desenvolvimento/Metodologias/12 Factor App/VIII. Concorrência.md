---
Date: 2024-10-25
---
[[12 - Factor App]]

![[Pasted image 20241025145654.png]]
**Na aplicação doze-fatores, processos são cidadãos de primeira classe.** Processos na aplicação doze-fatores utilizam fortes sugestões do modelo de processos UNIX para execução de serviços daemon, o desenvolvedor pode arquitetar a aplicação dele para lidar com diversas cargas de trabalho, atribuindo a cada tipo de trabalho a um _tipo de processo_. Por exemplo, solicitações HTTP podem ser manipuladas para um processo web, e tarefas background de longa duração podem ser manipuladas por um processo trabalhador.

