---
tags: []
Date: 2024-10-21
---
[[12 - Factor App]]

 Se existem várias bases de código, isto não é uma app – é um sistema distribuído. Cada componente do sistema é uma app, e cada uma pode individualmente ser compatível com os 12 fatores.

Múltiplas apps compartilhando uma base de código é uma violação dos 12 fatores.

Um repositório para todas as aplicações e uma violação.

A solução aqui é dividir o código compartilhado entre bibliotecas que podem ser incluídas através do [gerenciador de dependências](https://12factor.net/dependencies).


