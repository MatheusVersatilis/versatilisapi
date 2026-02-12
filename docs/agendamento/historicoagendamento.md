# Histórico de Agendamentos

Retorna todos os agendamentos realizados pelo usuário informado.

---

## Endpoint

`GET /api/Agendamento/HistoricoAgendamento`

---

## Query Parameters

| Parâmetro   | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| codUsuario | integer | Sim        | Código do usuário (paciente) |

---

## Exemplo de Requisição

```
GET /api/Agendamento/HistoricoAgendamento?codUsuario=1234
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
  },
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
    "Data": "2025-08-29",
    "Hora": "15:00",
    "Status": "PROCEDIMENTO MARCADO",
    "CodHorario": 45640,
    "CodAgendamento": 36435,
    "CodUsuario": 1234,
    "Paciente": "TESTE I",
    "CelularPaciente": "(11) 91111-1111",
    "TelefonePaciente": "",
    "BitTelemedicina": false,
    "Agendada": true,
    "Confirmada": false,
    "Aceita": false,
    "Cancelada": false
  },
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
    "Data": "2025-08-28",
    "Hora": "08:00",
    "Status": "PROCEDIMENTO MARCADO",
    "CodHorario": 45604,
    "CodAgendamento": 36434,
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
