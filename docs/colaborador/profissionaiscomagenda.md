# Listar Profissionais com Agenda

Retorna os profissionais que possuem agenda disponível para a especialidade informada.

Se `DataSelecionada` for informada, o retorno será filtrado para exibir apenas profissionais com disponibilidade na data especificada.

---

## Endpoint

`GET /api/Colaborador/ProfissionalAgenda`

---

## Query Parameters

| Parâmetro         | Tipo     | Obrigatório | Descrição |
|------------------|----------|------------|------------|
| CodEspecialidade | int      | Sim        | Código da especialidade |
| DataSelecionada  | datetime | Não        | Data específica para verificar disponibilidade (formato: YYYY-MM-DD) |

---

## Exemplo de Requisição

```
GET /api/Colaborador/ProfissionalAgenda?CodEspecialidade=1&DataSelecionada=2026-01-19
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
