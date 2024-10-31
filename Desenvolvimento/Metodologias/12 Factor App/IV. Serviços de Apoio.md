---
Date: 2024-10-21
---
[[12 - Factor App]]

Um _serviço de apoio_ é qualquer serviço que o app consuma via rede como parte de sua operação normal. Exemplos incluem armazenamentos de dados (como [MySQL](http://dev.mysql.com/) ou [CouchDB](http://couchdb.apache.org/)), sistemas de mensagens/filas (tais como [RabbitMQ](http://www.rabbitmq.com/) ou [Beanstalkd](https://beanstalkd.github.io/)), serviços SMTP para emails externos (tais como [Postfix](http://www.postfix.org/)), e sistemas de cache (tais como [Memcached](http://memcached.org/)).

**O código para um app doze-fatores não faz distinção entre serviços locais e de terceiros.** Para o app, ambos são recursos anexados, acessíveis via uma URL ou outro localizador/credenciais na [config](https://12factor.net/pt_br/config). Um [deploy](https://12factor.net/pt_br/codebase) do app doze-fatores deve ser capaz de trocar um banco de dados MySQL por um gerenciado por terceiros (tais como [Amazon RDS](http://aws.amazon.com/rds/)) sem realizar quaisquer mudanças no código do app. Da mesma forma, um servidor local SMTP poderia ser trocado por um serviço de terceiros (tais como Postmark) sem as mudanças em código. Em ambos os casos, apenas o identificador de recurso precisa mudar.

Cada serviço de apoio distinto é um _recurso_. Por exemplo, um banco MySQL é um recurso; dois bancos MySQL (usados para sharding na camada da aplicação) qualificam como dois recursos distintos. O app doze-fatores trata tais bancos como _recursos anexados_, o que indica seu baixo acoplamento ao deploy que ele está anexado.

![Um deploy de produção anexado a quatro serviços de apoio.](https://12factor.net/images/attached-resources.png)

Recursos podem ser anexados e desanexados a deploys à vontade. Por exemplo, se o banco de dados do app não está funcionando corretamente devido a um problema de hardware, o administrador do app pode subir um novo servidor de banco de dados restaurado de um backup recente. O atual banco de produção pode ser desanexado, e o novo banco anexado – tudo sem nenhuma mudança no código.