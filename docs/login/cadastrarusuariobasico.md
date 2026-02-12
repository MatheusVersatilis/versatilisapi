# Cadastrar Novo Usuário Básico

Realiza o cadastro de um novo usuário básico (paciente).

Este endpoint exige apenas:
- Nome do paciente
- Número de celular ou telefone

---

## Endpoint

`POST /api/Login/CadastrarUsuarioBasico`

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
  "Celular": "11922123324"
}
```

---

## Campos do Body

| Campo   | Tipo   | Obrigatório | Descrição |
|----------|--------|------------|------------|
| Nome     | string | Sim        | Nome do paciente |
| Celular  | string | Sim*       | Número de celular do paciente |

\* Deve ser informado ao menos Celular ou Telefone.

---

## Response 200 - Sucesso

```json
{
  "CodUsuario": "1",
  "Nome": "Teste",
  "CPF": null,
  "Email": null,
  "Senha": null,
  "DtNasc": null,
  "Sexo": null,
  "Telefone": null,
  "Celular": "11922123324",
  "CEP": null,
  "Endereco": null,
  "Numero": null,
  "Complemento": null,
  "Bairro": null,
  "Cidade": null,
  "FacebookID": null,
  "SemanasGestacao": null,
  "DiasGestacao": null,
  "DtParto": null,
  "CodPlanos": [1, 2, 3, 4]
}
```

---

## Observações

- O usuário é criado como **básico**, podendo posteriormente complementar os demais dados.
- O campo `CodPlanos` retorna os planos vinculados ao usuário.
