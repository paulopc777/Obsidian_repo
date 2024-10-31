---
Date: 2024-10-22
---
[[12 - Factor App]]

- - **O _estágio de construção_** é uma transformação que converte um repositório de código em um pacote executável conhecido como _construção_. Usando uma versão do código de um commit especificado pelo processo de desenvolvimento, o estágio de construção obtém e fornece [[II. Dependências]] e compila binários e ativos.
- **O _estágio de lançamento_** pega a construção produzida pelo estágio de construção e a combina com a atual [[III. Configurações]] do deploy. O _lançamento_ resultante contém tanto a construção quanto a configuração e está pronta para execução imediata no ambiente de execução.
- **O _estágio de execução_** roda o app no ambiente de execução, através do início de alguns dos [processos](https://12factor.net/pt_br/processes) do app com um determinado lançamento.


![[Pasted image 20241022081759.png]]

