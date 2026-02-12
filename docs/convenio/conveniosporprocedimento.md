# Listar Convênios por Procedimento

Retorna os convênios disponíveis no portal de acordo com a unidade e o procedimento informados.

---

## Endpoint

`GET /api/Convenio/PlanosProcedimento`

---

## Query Parameters

| Parâmetro        | Tipo | Obrigatório | Descrição |
|-----------------|------|------------|------------|
| codUnidade      | int  | Sim        | Código da unidade |
| codProcedimento | int  | Sim        | Código do procedimento |

---

## Exemplo de Requisição

```
GET /api/Convenio/PlanosProcedimento?codUnidade=1&codProcedimento=1
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
