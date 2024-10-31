---
Date: 2024-10-23
tags:
  - Arquitetura
---
![[Pasted image 20241023201746.png]]

## Oque e

A Ideia e dividir a aplica de modo a separar os elemento internos dos elemento internos tornado os independes

**Camada Azul :**

- Frameworks
- Bibliotecas
- UI

**Verde :**

Adapta a camada azul para as duas subsequentes

**Vermelho :**
**Use Casse**

Não deve conversar com camas externas

Classes Independentes
  - Handler
  - Service

**Setas :**
As Entidades não conhecem o Use cases logo controles não conhece Use casse etc...


**Objetivos :**

- Facilidade de teste
- Independência de Frameworks
- Independência de UI
- Independência de Banco de dados

