# Listar Unidade por Código

Retorna os dados da unidade com base no código informado.

---

## Endpoint

`GET /api/Unidade/Unidade`

---

## Query Parameters

| Parâmetro   | Tipo | Obrigatório | Descrição |
|------------|------|------------|------------|
| codUnidade | int  | Sim        | Código da unidade |

---

## Exemplo de Requisição

```
GET /api/Unidade/Unidade?codUnidade=1
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
{
  "CodUnidade": 1,
  "NomeUnidade": "CLÍNICA VERSATILIS"
}
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas unidades cadastradas."
}
```
