# Listar Profissionais por Nome

Retorna os profissionais com base no nome informado.

---

## Endpoint

`GET /api/Colaborador/Profissional`

---

## Query Parameters

| Parâmetro        | Tipo   | Obrigatório | Descrição |
|------------------|--------|------------|------------|
| nomeColaborador  | string | Sim        | Nome (ou parte do nome) do profissional |

---

## Exemplo de Requisição

```
GET /api/Colaborador/Profissional?nomeColaborador=PROFISSIONAL
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
    "CodColaborador": 1,
    "Nome": "PROFISSIONAL TESTE",
    "Procedimentos": [
      {
        "CodProcedimento": 1,
        "NomeProcedimento": "PROCED EXEMPLO"
      }
    ]
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados profissionais para o nome informado."
}
```
