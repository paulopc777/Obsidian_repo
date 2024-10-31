---
Date: 2024-10-24
---
[Video](https://www.youtube.com/watch?v=ww3e1PXbCQU)
35:15 / 1:29:32

![[Pasted image 20241024075043.png]]
![[Pasted image 20241024075310.png]]
## Concorrência & Paralelismo 

**Concorrência**
**4 clientes**
Um cliente -> Pedido -> Processado = Latência | 1s
Um cliente -> Pedido -> Processado = Latência | 1s
Um cliente -> Pedido -> Processado = Latência | 1s
Um cliente -> Pedido -> Processado = Latência | 1s
Tempo total = 4s

**Paralelismo**
**4 clientes**
Um cliente -> Pedido -> Processado = Latência | 1s | Thread 1
Um cliente -> Pedido -> Processado = Latência | 1s | Thread 2
Um cliente -> Pedido -> Processado = Latência | 1s | Thread 3
Um cliente -> Pedido -> Processado = Latência | 1s | Thread 4
Tempo total = 1s

![[Pasted image 20241024075647.png]]


Quanto mais Thread trabalhando ao mesmo tempo maior os recursos usados quando não a recurso as Thread esperam ate que recursos estejam livres bloqueando as Thread.

	Littles`s Law
[Little](https://en.wikipedia.org/wiki/Little%27s_law)

![[Pasted image 20241024080241.png]]
![[Pasted image 20241024080341.png]]

## Como implementar Concorrência

[Call-back Hell](http://callbackhell.com/)

![[Pasted image 20241024081643.png]]
