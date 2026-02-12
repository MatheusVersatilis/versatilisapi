# Listar Consultas Agendadas

Retorna as consultas do usuário de acordo com os filtros informados.

---

## Endpoint

`GET /api/Agendamento/ConsultasAgendadas`

---

## Query Parameters

| Parâmetro        | Tipo | Obrigatório | Descrição |
|------------------|------|------------|------------|
| codUsuario       | int  | Sim        | Código do usuário |
| bitAgendadas     | bool | Sim        | Padrão: `true`. Retorna agendadas (`true`) ou não agendadas (`false`) |
| bitAceitas       | bool | Não        | Filtra por aceitas (`true`) ou não aceitas (`false`). Se não informado, não aplica filtro |
| bitConfirmadas   | bool | Não        | Padrão: `false`. Filtra por confirmadas (`true`) ou não confirmadas (`false`) |
| bitCanceladas    | bool | Não        | Padrão: `false`. Filtra por canceladas (`true`) ou não canceladas (`false`) |

---

## Exemplo de Requisição

```
GET /api/Agendamento/ConsultasAgendadas?codUsuario=1&bitAgendadas=true&bitConfirmadas=false
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

> Recomenda-se utilizar o padrão de data `YYYY-MM-DD`.

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas consultas agendadas."
}
```
