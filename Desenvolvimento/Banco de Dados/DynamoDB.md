---
tags:
  - Database
---

[Site](https://vinicius-roc.medium.com/dynamodb-o-que-voc%C3%AA-precisa-saber-antes-de-usar-1bcad8d31787)

DynamoDB é um banco NoSQL totalmente gerenciado pela AmazonWS, de forma que não precisamos criar a infraestrutura para tal, como faríamos utilizando o NodeJS ou o Cassandra.

Ele é orientado a Documento ou Chave-valor. Melhor dizendo é um banco Chave-valor que suporta o tipo de dado Documento, onde você pode armazenar um JSON.

É rápido, consistente, possui controle de acesso e _event driven programming_, ou seja, as alterações nele disparam eventos que podem ser observados e utilizados em algum serverless como Lambda.