# Listar Horários por Colaborador

Retorna os horários registrados para o colaborador informado.

---

## Endpoint

`GET /api/Agenda/Datas`

---

## Regras de Filtragem

- **Somente DataInicial informada**: retorna os horários apenas da data especificada.
- **Somente DataFinal informada**: retorna os horários até a data especificada.
- **Nenhuma data informada**: retorna os horários dentro do período padrão de 2 meses.
- **DataInicial e DataFinal informadas**: retorna os horários dentro do intervalo selecionado.

---

## Query Parameters

| Parâmetro       | Tipo     | Obrigatório | Descrição |
|---------------|----------|------------|------------|
| codColaborador | int      | Sim        | Código do colaborador |
| codUsuario     | int      | Não        | Código do usuário |
| dataInicial    | date     | Não        | Data inicial no formato `YYYY-MM-DD` |
| dataFinal      | date     | Não        | Data final no formato `YYYY-MM-DD` |

> Observação: As datas devem ser informadas no padrão ISO 8601 (`YYYY-MM-DD`).

---

## Exemplo de Requisição

```
GET /api/Agenda/Datas?codColaborador=1&codUsuario=1&dataInicial=2025-12-01&dataFinal=2025-12-31
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
    "CodHorario": 1,
    "Data": "2023-12-12",
    "Hora": "08:00",
    "CodEspecialidade": 10,
    "NomeEspecialidade": "Psicologia",
    "PermiteConsulta": true,
    "PermiteProcedimento": true,
    "Procedimentos": [
      {
        "CodProcedimento": 1,
        "NomeProcedimento": "TERAPIA"
      }
    ]
  },
  {
    "CodHorario": 2,
    "Data": "2023-12-12",
    "Hora": "09:00",
    "CodEspecialidade": 10,
    "NomeEspecialidade": "Psicologia",
    "PermiteConsulta": true,
    "PermiteProcedimento": true,
    "Procedimentos": [
      {
        "CodProcedimento": 1,
        "NomeProcedimento": "TERAPIA"
      }
    ]
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas datas disponíveis para o colaborador informado."
}
```
