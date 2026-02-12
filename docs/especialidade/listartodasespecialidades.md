# Listar Especialidades

Retorna a lista de especialidades disponíveis no sistema.

## Endpoint

`GET /api/Especialidade/Especialidades`

---

## Query Parameters

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|------------|-----------|
| codPlano  | int  | Não        | Código do plano para filtrar as especialidades |

### Exemplo

```
GET /api/Especialidade/Especialidades?codPlano=7
```

---

## Headers

| Header        | Valor            |
|---------------|------------------|
| Authorization | Bearer {token}   |

### Exemplo

```
Authorization: Bearer e6804ca35ff03261f5a1967aeb7e29f
```

---

## Response 200 - Sucesso

```json
[
  {
    "NomeEspecialidade": "ACUPUNTURA",
    "CodEspecialidade": 1,
    "Valor": "",
    "Descricao": "TESTE"
  },
  {
    "NomeEspecialidade": "ALERGOLOGIA",
    "CodEspecialidade": 2,
    "Valor": "",
    "Descricao": "TESTE"
  },
  {
    "NomeEspecialidade": "CARDIOLOGIA",
    "CodEspecialidade": 3,
    "Valor": "",
    "Descricao": "TESTE"
  },
  {
    "NomeEspecialidade": "CLÍNICA GERAL",
    "CodEspecialidade": 4,
    "Valor": "",
    "Descricao": "TESTE"
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas especialidades cadastradas."
}
```
