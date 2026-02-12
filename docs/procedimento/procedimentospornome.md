# Listar Procedimentos por Nome

Retorna os procedimentos com base no nome informado.

Caso o parâmetro `nomeProcedimento` esteja vazio, todos os procedimentos cadastrados no sistema serão listados.

---

## Endpoint

`GET /api/Procedimento/Procedimentos`

---

## Query Parameters

| Parâmetro         | Tipo    | Obrigatório | Padrão | Descrição |
|------------------|---------|------------|--------|------------|
| nomeProcedimento | string  | Não        | —      | Nome (ou parte do nome) do procedimento |
| codPlano         | int     | Não        | —      | Código do plano para filtro |
| filtrarPortal    | boolean | Não        | true   | Quando `true`, retorna apenas procedimentos disponíveis no portal |

---

## Exemplo de Requisição

```
GET /api/Procedimento/Procedimentos?nomeProcedimento=teste&codPlano=7&filtrarPortal=true
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
    "NomeProcedimento": "Teste",
    "CodEspecialidade": 2,
    "NomeEspecialidade": "Especialidade Teste",
    "BitExame": false
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
