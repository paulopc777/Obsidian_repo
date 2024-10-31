---
Date: 2024-10-22
---
### Exporte serviços via vínculo de portas

**O aplicativo doze-fatores é completamente auto-contido** e não depende de injeções de tempo de execução de um servidor web em um ambiente de execução para criar um serviço que defronte a web. O app web **exporta o HTTP como um serviço através da vínculação a uma porta**, e escuta as requisições que chegam na mesma.

Note que a abordagem de vincular portas significa que um app pode se tornar o [serviço de apoio](https://12factor.net/pt_br/backing-services) para um outro app, provendo a URL do app de apoio como um identificador de recurso na [configuração](https://12factor.net/pt_br/config) para o app consumidor.