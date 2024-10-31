Servidor Web soctes


---
# Login 

POST 
api.monitchat.com/api/v1/auth/login


```JSON
{
"username":"",
"password":"ideiad@2022*",
"redirect":false,
"email":"suporte@institutoideias.com.br"
}
```

# Add Intenções

POST
api.monitchat.com/api/v1/trigger

```JSON 

{"intents":[
	{
		"description":"vasdasd",
		"final_intent":false,
		"use_button":false,
		"button_body":"",
		"button_footer":"",
		"button_header":"",
		"buttons":[],
		"accounts":[],
		"action":{
				"action_type":"",
				  "message":"",
				  "user_id":"",
				  "department_id":"",
				  "ticket_status_id":"",
				  "get_url":"",
				  "file_name":"",
				  "mime_type":"",
				  "file_data":"",
				  "get_fields":"",
				  "get_results":"",
				  "post_url":"",
				  "auth_url":"",
				  "json_data_request":"",
				  "token_field_name":"",
				  "post_fields":"",
				  "headers":"",
				  "headers_value":""
			}
		}
],"replies":[
		{
			"description":"asdasdasd",
			"weight":""
		}
	]
}

```

```JSON
"description":"@topic Menu @intent inicio\n",
```

---

**OPTIONS**

/api/v1/trigger/115609
/api/v1/trigger/115610

**DELETE** 

_ID da Intenção_

/api/v1/trigger/==115610==

Authorization: Bearer Token

**Header**

```JSON
Access-Control-Request-Method: DELETE
```