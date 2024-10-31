---
Date: 2024-10-23
---
[[Clean Architecture]]

## Use Case

![[Pasted image 20241023205555.png]]

**Input Boyndaty - DTO**
**Input Output - DTO**

Classes DTO para entrada de retorno do Use casse tornando invisível para as classes externas.

```typescript
// Use case
function handle(InputBoundaty:InputBoundaty):OutputBoundaty {
	// Implementacao
}
```

dados dos DTOS devem ser mais primitivos possíveis como String, Number etc...

