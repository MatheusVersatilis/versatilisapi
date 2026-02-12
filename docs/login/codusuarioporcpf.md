# Listar CodUsuario pelo CPF

Retorna o código do usuário com base no CPF informado.

---

## Endpoint

`GET /api/Login/CodUsuario?CPF={CPF}`

---

## Query Parameters

| Parâmetro | Tipo   | Obrigatório | Descrição                |
|-----------|--------|------------|-------------------------|
| CPF       | string | Sim        | CPF do usuário           |

---

## Headers

| Header        | Valor |
|---------------|-------|
| Authorization | Bearer {token} |

### Exemplo

```
Authorization: Bearer TokenObtidoAnteriormente
```

---

## Response 200 - Sucesso

```json
{
  "CodUsuario": 1
}
```

---

## Response 404 - Não encontrado

```json
{
  "Usuário não encontrado"
}
```

---

## Observações

- Retorna apenas o código do usuário vinculado ao CPF informado.
- Se o CPF não existir, retorna 404.
