# Listar Procedimentos pelo TUSS

Retorna os procedimentos com base no código TUSS informado.

---

## Endpoint

`GET /api/Procedimento/Procedimentos`

---

## Query Parameters

| Parâmetro | Tipo   | Obrigatório | Descrição |
|------------|--------|------------|------------|
| TUSS       | string | Sim        | Código TUSS do procedimento |

---

## Exemplo de Requisição

```
GET /api/Procedimento/Procedimentos?TUSS=123
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
    "CodProcedimento": 1,
    "NomeProcedimento": "Teste"
  },
  {
    "CodProcedimento": 2,
    "NomeProcedimento": "Teste2"
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados procedimentos cadastrados."
}
```
