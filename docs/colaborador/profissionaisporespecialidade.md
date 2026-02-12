# Listar Profissionais por Especialidade

Retorna os profissionais disponíveis para a especialidade informada.

---

## Endpoint

`GET /api/Colaborador/Profissional`

---

## Query Parameters

| Parâmetro         | Tipo | Obrigatório | Descrição |
|------------------|------|------------|------------|
| CodEspecialidade | int  | Sim        | Código da especialidade |

---

## Exemplo de Requisição

```
GET /api/Colaborador/Profissional?CodEspecialidade=1
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
  "message": "Não foram encontrados profissionais disponíveis para a especialidade informada."
}
```
