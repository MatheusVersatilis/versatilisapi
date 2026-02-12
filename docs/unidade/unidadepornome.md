# Listar Unidade por Nome

Retorna os dados da unidade com base no nome informado.

---

## Endpoint

`GET /api/Unidade/UnidadePorNome`

---

## Query Parameters

| Parâmetro    | Tipo   | Obrigatório | Descrição |
|-------------|--------|------------|------------|
| NomeUnidade | string | Sim        | Nome (ou parte do nome) da unidade |

---

## Exemplo de Requisição

```
GET /api/Unidade/UnidadePorNome?NomeUnidade=CLÍNICA
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
  "NomeUnidade": "CLÍNICA VERSATILIS",
  "Endereco": "RUA TESTE 123 BLOCO B, 02031-007 - SP"
}
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas unidades cadastradas."
}
```
