# Listar Consultas Agendadas por Período

Retorna as consultas dentro do intervalo de datas informado, aplicando os filtros de status quando especificados.

---

## Endpoint

`GET /api/Agendamento/ConsultasAgendadasPorData`

---

## Query Parameters

| Parâmetro        | Tipo     | Obrigatório | Descrição |
|------------------|----------|------------|------------|
| dataInicial      | datetime | Sim        | Data inicial no formato `YYYY-MM-DDTHH:mm:ss` |
| dataFinal        | datetime | Sim        | Data final no formato `YYYY-MM-DDTHH:mm:ss` |
| bitAgendadas     | bool     | Sim        | Padrão: `true`. Retorna agendadas (`true`) ou não agendadas (`false`) |
| bitAceitas       | bool     | Não        | Filtra por aceitas (`true`) ou não aceitas (`false`). Se não informado, não aplica filtro |
| bitConfirmadas   | bool     | Não        | Padrão: `false`. Filtra por confirmadas (`true`) ou não confirmadas (`false`) |
| bitCanceladas    | bool     | Não        | Padrão: `false`. Filtra por canceladas (`true`) ou não canceladas (`false`) |

> Recomenda-se utilizar o padrão ISO 8601 (`YYYY-MM-DDTHH:mm:ss`).

---

## Exemplo de Requisição

```
GET /api/Agendamento/ConsultasAgendadasPorData?dataInicial=2023-12-12T00:00:00&dataFinal=2023-12-12T23:59:59&bitAgendadas=true
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
    "CodEspecialidade": 5,
    "Especialidade": "CARDIOLOGIA",
    "CodProcedimento": 2,
    "Procedimento": "ECOCARDIOGRAMA",
    "CodUnidade": 1,
    "Unidade": "UNIDADE 1",
    "CodColaborador": 4,
    "Medico": "MARCELO ALVES",
    "CodConvenio": 2007,
    "Convenio": "PARTICULAR",
    "CodPlano": 3011,
    "Plano": "SEM NOTA FISCAL",
    "Data": "2025-08-30",
    "Hora": "15:30",
    "Status": "PROCEDIMENTO MARCADO",
    "CodHorario": 43202,
    "CodAgendamento": 36436,
    "CodUsuario": 1234,
    "Paciente": "TESTE I",
    "CelularPaciente": "(11) 91111-1111",
    "TelefonePaciente": "",
    "BitTelemedicina": false,
    "Agendada": true,
    "Confirmada": false,
    "Aceita": false,
    "Cancelada": false
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas consultas agendadas."
}
```
