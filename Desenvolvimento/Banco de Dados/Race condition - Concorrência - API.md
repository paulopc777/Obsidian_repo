---
tags:
  - Database
---


![[Pasted image 20241020115342.png]]

Em um cenário onde temos um bando de dados, com informações de saldo.
Um API expõe os dados para os Clientes.

Imagine o cenário onde 2 Clientes fazem a requisição para mesma tabela ao mesmo tempo.

Temos um cenário de concorrência.

Duas requisições correndo para ver quem finaliza sua operação primeiro.

![[Pasted image 20241020115744.png]]
Nesse cenário a API faz duas consulta quase simultâneas no banco de dados. 

O retorno e valido para operação , em ambas operações o saldo e valido para debito , mas...

Um saldo de Usuário não pode ser negativo , mas no exato momento isso ira acontecer após o update como o mesmo será executado 2 vezes temos saldo = 5 , saldo = 5 - 5 = 0 , **segunda chamada** saldo = 0 - 5  = **-5**

_Race condition_ é um problema comum que acontece em programação concorrente, onde duas threads modificam o mesmo recurso simultaneamente, podendo gerar resultados inesperados.

# Como resolver o problema?


[Optimistic vs. Pessimistic locking](https://stackoverflow.com/questions/129329/optimistic-vs-pessimistic-locking)

**Pessimistic Locking**:

é quando você bloqueia o registro para seu uso exclusivo até que tenha terminado de usá-lo.

```SQL
SELECT FOR UPDATE * FROM      tabela WHERE id = 1
```

```SQL
UPDATE tabela SET saldo = saldo - 5 WHERE id = 1
```

Permitir que apenas uma compra debite da conta bancária por vez.

**Optimistic Locking**:

 uma estratégia onde você lê um registro, toma nota de um número de versão (outros métodos para fazer isso envolvem datas, timestamps ou checksums/hashes) e verifica se a versão não mudou antes de gravar o registro de volta. Quando você grava o registro de volta, você filtra a atualização na versão para ter certeza de que ela é atômica. (ou seja, não foi atualizada entre quando você verifica a versão e grava o registro no disco) e atualiza a versão em um hit.

```SQL
SELECT saldo,create_at FROM tabela WHERE id=1
```

```SQL
UPDATE saldo SET saldo = saldo - 5 WHERE id = 1 AND version = 1
```