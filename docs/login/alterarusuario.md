# Alterar Dados do Usuário

Atualiza os dados cadastrais do usuário (paciente).

---

## Endpoint

`PUT /api/Login/AlterarUsuario`

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

## Body (application/json)

```json
{
  "Nome": "Teste",
  "CPF": "111.111.111-11",
  "Email": "teste@teste.com.br",
  "Senha": "e10adc3949ba59abbe56e057f20f883e",
  "DtNasc": "2017-01-12",
  "Sexo": "M",
  "Telefone": "1122322112",
  "Celular": "11922123324",
  "CEP": "08635709",
  "Endereco": "Rua de Teste",
  "Numero": "12",
  "Complemento": "Teste",
  "Bairro": "Teste",
  "Cidade": "SUZANO",
  "SemanasGestacao": "1",
  "DiasGestacao": "1",
  "DtParto": "2023-02-10",
  "CodPlano": "1",
  "NumCarteirinha": "123",
  "CodPlanos": [1, 2, 3, 4]
}
```

---

## Campos do Body

Todos os campos
