**POST [Link](https://api-v2.monitchat.com/api/v1/template/send)**

**Req params:**

```

{
    "token": "48da61c8-8453-61b807660e30",
    "template": {
        "category": "UTILITY",
        "components": [
            {
                "parameters": [
                    {
                        "type": "text",
                        "text": "tESTE"
                    }
                ],
                "type": "body",
                "format": null
            },
            {
                "parameters": [],
                "type": "buttons",
                "format": null
            }
        ],
        "id": "RvRCWsCOLwWsNfLGTwU5WT",
        "name": "cirurgias",
        "namespace": "1402b301_c8b9_41c1_82a3_602e350b16b0",
        "data": {},
        "message": ""
    },
    "erp_ticket_id": "<opcional>",
    "phone_number": "5527999863591",
    "accountNumber": "5527998927886"
}
```


[CriarDepartamento](https://api-v2.monitchat.com/api/v1/department)

```
1. {id: "", active: true, company_id: "", created_at: "", deleted_at: "",…}

1. active: true
2. bot_message: ""
3. company_id: ""
4. created_at: ""
5. created_by: ""
6. deleted_at: ""
7. department_id: ""
8. departments: ""
9. description: "Aracruz, Itapemirim, Linhares, Marataízes."
10. filial: []
11. id: ""
12. is_queueable: false
13. last_ticket_assigned_on: ""
14. menu: ""
15. name: "Espirito Santo"
16. overflow_department_id: ""
17. overflow_user_id: 6286
18. send_campaing: true
19. show_on_bot: true
20. status_id: 4609
21. updated_at: ""
22. use_wallet: ""
23. user: ""
24. users: [6284]
25. webhook_active: true
```