---
Date: 2024-10-21
---
[[12 - Factor App]]

Aplicações às vezes armazenam as configurações no código como constantes. 
Isto é uma violação da doze-fatores, a qual exige uma **estrita separação entre configuração e código**. Configuração varia substancialmente entre deploys.

**A aplicação doze-fatores armazena configuração em _variáveis de ambiente_** (muitas vezes abreviadas para _env vars_ ou _env_).

Em uma aplicação doze-fatores, env vars são controles granulares, cada um totalmente ortogonal às outras env vars. Elas nunca são agrupadas como “environments”, mas em vez disso são gerenciadas independentemente para cada deploy. Este é um modelo que escala sem problemas à medida que o app naturalmente se expande em muitos deploys durante seu ciclo de vida.