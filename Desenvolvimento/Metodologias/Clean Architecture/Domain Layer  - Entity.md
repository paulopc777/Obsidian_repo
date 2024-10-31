---
Date: 2024-10-23
---
[[Clean Architecture]]

Entidade pode ser traduzida com Interfaces para as classe , tipadas.
Validando as entidades, ou os Objetos.

Regas de dados como Age , E-mail devem ser validadas nessa camada
```typescript
	function setAge(Age:numeber){
		if(Age > 18){
			this.Age = Age;
			return true
		}
		// Usuario nao pode ser de menor !
		return false
	}
```

**Value Objects**

Adicionando a regra de validação dentro do type E-mail, classe ou função  

```typescript
interface User {
	Email:Email;
}
```
