# Agendamentos por ID

Retorna os detalhes de um agendamento específico a partir do seu identificador.

---

## Endpoint

`GET /api/Agendamento/AgendamentoPorId`

---

## Query Parameters

| Parâmetro       | Tipo    | Obrigatório | Descrição |
|----------------|---------|------------|------------|
| codAgendamento | integer | Sim        | Código do agendamento |

---

## Exemplo de Requisição

```
GET /api/Agendamento/AgendamentoPorId?codAgendamento=36456
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
  "CodEspecialidade": 5,
  "Especialidade": "CARDIOLOGIA",
  "CodProcedimento": null,
  "Procedimento": "",
  "CodUnidade": 1,
  "Unidade": "UNIDADE 1",
  "CodColaborador": 4,
  "Medico": "MARCELO ALVES",
  "CodConvenio": 4,
  "Convenio": "SAUDE DA COLUNA",
  "CodPlano": 6,
  "Plano": "PARTICULAR",
  "Data": "2025-10-22",
  "Hora": "11:00",
  "Status": "CONSULTA CANCELADA PELO PACIENTE",
  "CodHorario": 46593,
  "CodAgendamento": 36456,
  "CodUsuario": 1234,
  "Paciente": "TESTE I",
  "CelularPaciente": "(11) 91111-1111",
  "TelefonePaciente": "",
  "BitTelemedicina": false,
  "Agendada": false,
  "Confirmada": false,
  "Aceita": false,
  "Cancelada": true
}
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Agendamento não encontrado."
}
```
