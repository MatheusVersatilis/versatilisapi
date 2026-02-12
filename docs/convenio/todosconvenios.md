# Listar Todos os Convênios

Retorna todos os convênios disponíveis no sistema.

---

## Endpoint

`GET /api/Convenio/Planos`

---

## Query Parameters

| Parâmetro      | Tipo    | Obrigatório | Descrição |
|---------------|---------|------------|------------|
| filtrarPortal | boolean | Não        | Padrão: `true`. Quando `true`, retorna apenas convênios disponíveis no portal |

---

## Exemplo de Requisição

```
GET /api/Convenio/Planos?filtrarPortal=true
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
    "CodConvenio": 2,
    "NomeConvenio": "PARTICULAR",
    "Planos": [
      {
        "CodPlano": 2,
        "NomePlano": "PARTICULAR"
      }
    ]
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados convênios disponíveis."
}
```
