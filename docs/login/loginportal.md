## Login Portal
`POST /api/Login/CadastrarUsuario`

Este endpoint é reponsavél por realizar o login do paciente.

---

## Headers

| Nome | Obrigatório | Descrição |
|-----|------------|-----------|
| Authorization | Sim | Bearer Token obtido anteriormente |

---

## Request Body

```json
{
	"Login": "808.379.920-36",
	"Senha": "1234"
}
```

## Response 200
```json
{
    "CodUsuario": 5012,
    "Nome": "TESTE VINICIUS",
    "CPF": "80837992036",
    "Email": "",
    "Senha": "1234",
    "DtNasc": "1993-08-03T00:00:00",
    "Telefone": "",
    "Celular": "(11) 11111-1111",
    "CEP": "",
    "Endereco": "",
    "Numero": "",
    "Complemento": "",
    "Bairro": "",
    "Cidade": "",
    "Sexo": "M",
    "FacebookID": "",
    "SemanasGestacao": null,
    "DiasGestacao": null,
    "DtParto": null,
    "CodPlano": 9,
    "CodPlanos": [
		9,
		3011
    ],
    "NumCarteirinha": null
}
```

## Response 404 
```json
            {
                "Usuário não encontrado."  
            }
```