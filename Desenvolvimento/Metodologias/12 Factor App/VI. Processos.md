---
Date: 2024-10-22
---
[[12 - Factor App]]

**Execute a aplicação como um ou mais processos que não armazenam estado**

**Processos doze-fatores são stateless(não armazenam estado) e [share-nothing](http://en.wikipedia.org/wiki/Shared_nothing_architecture).** Quaisquer dados que precise persistir deve ser armazenado em um serviço de apoio stateful(que armazena o seu estado), tipicamente uma base de dados.

Alguns sistemas web dependem de [“sessões persistentes”](http://en.wikipedia.org/wiki/Load_balancing_%28computing%29#Persistence) – ou seja, fazem cache dos dados da sessão do usuário na memória do processo da aplicação, esperando futuras requisições do mesmo visitante para serem encaminhadas para o mesmo processo. Sessões persistentes são uma violação do doze-fatores e nunca devem ser utilizadas ou invocadas. Dados do estado da sessão são bons candidatos para um datastore que oferece tempo de expiração, tal como [Memcached](http://memcached.org/) ou [Redis](http://redis.io/).