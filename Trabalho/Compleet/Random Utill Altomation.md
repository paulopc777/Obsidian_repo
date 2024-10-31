
## Valores 

Serviço = 0.03 USD - 0,15 BRL
Utilitários = 0.035 USD - 0,175 BRL 
Marketing = $ 0.0625 USD - 0,3125 BRL
## Chamadas de Função

Não usa Botão 
_Name topic:_

```
@sys.start_topic Name
```

Tipa o inicio do código como _**Identificador**_  do mesmo.

Inicio de chamada e final de chamada : 

```
@sys.opt
```

Requerimento de retorno "array": 

```
@sys.array_must(text)
```


Termino do tópico :

```
@sys.end_topic
```


```
@sys.end_topic
```



P1 : Nome automação. 
P2: **Identificador** de Contexto.
P3 : Inter padrão de inicio .

```
_P1_ @topic _P2_ @intent _P3_
```

**P1** : Chamada de outro contexto 

```
@topic _P1_
```


_Chamada padrão singular de tipagem da chamada em termos._
**Uso em todo envio **

```
@topic random
```


_Chamada simples tipagem de inicio de chamada_

```
@intent inicio
```


**Variáveis de ambiente **
_Variável criado no menu de Variáveis_

```
@user.set{Var}
```

```
@user.formal{Var}
```

---
## Contexto Conversas 

*Atribute*

**Nome do Contato**

```
{contact_name}
```


**Saudação**

```
{greeting}!
```
_Exemplo  bom dia _
**Return:**
Bom dia ! etc ...


**Node da Empresa contactante**


 ```
 {{Nome_Da_Empresa}},
```

## Ideia de Criação 

**Chamada de Intenção**

```
@topic Name_topic @intent inicio
```

---

@sys.opt @sys.array_must(pilar,marechal deodoro) @sys.opt

![[Pasted image 20240703134747.png]]

---
### Ação de post

**Url :**

> Primeiro parâmetro =  Content-type ,
> Segundo parâmetro = application/json 
