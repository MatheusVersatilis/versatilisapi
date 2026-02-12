# Listar Convênios por Especialidade

Retorna os convênios disponíveis no portal de acordo com a unidade e especialidade informadas.

---

## Endpoint

`GET /api/Convenio/Planos`

---

## Query Parameters

| Parâmetro         | Tipo | Obrigatório | Descrição |
|------------------|------|------------|------------|
| codUnidade       | int  | Sim        | Código da unidade |
| codEspecialidade | int  | Sim        | Código da especialidade |

---

## Exemplo de Requisição

```
GET /api/Convenio/Planos?codUnidade=1&codEspecialidade=1
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
    "CodPlano": 2,
    "NomeConvenio": "PARTICULAR",
    "NomePlano": "PARTICULAR"
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
