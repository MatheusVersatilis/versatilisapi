# Dados do Usuário por CPF

Retorna os dados cadastrais do usuário com base no CPF informado.

---

## Endpoint

`GET /api/Login/DadosUsuarioPorCPF`

---

## Query Parameters

| Parâmetro | Tipo   | Obrigatório | Descrição |
|------------|--------|------------|------------|
| UserCPF    | string | Sim        | CPF do usuário |

---

## Exemplo de Requisição

```
GET /api/Login/DadosUsuarioPorCPF?UserCPF=123.456.789-10
```

---

## Headers

| Header        | Valor |
|---------------|--------|
| Authorization | Bearer {token} |

### Exemplo

```
Authorization: Bearer TokenObtidoAnteriormente
```

---

## Response 200 - Sucesso

```json
[
  {
    "CodUsuario": "1",
    "Nome": "Teste",
    "CPF": "111.111.111-11",
    "Email": "teste@teste.com.br",
    "Senha": "123456",
    "DtNasc": "10/08/2017",
    "Sexo": "M",
    "Telefone": "1122322112",
    "Celular": "11922123324",
    "CEP": "08635709",
    "Endereco": "Rua de Teste",
    "Numero": "12",
    "Complemento": "Teste",
    "Bairro": "Teste",
    "Cidade": "SUZANO",
    "FacebookID": " ",
    "Planos": [1, 2, 3]
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "Usuário não encontrado."
}
```

---

## Observações

- O CPF deve estar cadastrado na base de dados.
- O retorno inclui os planos vinculados ao usuário no campo `Planos`.
