# Marcar Agendamento

Realiza a confirmação e criação de um agendamento para o paciente.

---

## Endpoint

`POST /api/Agenda/ConfirmarAgendamento`

---

## Regras

- Caso **CodHorario = 0**, o sistema tentará agendar utilizando o campo **Data**, desde que exista horário livre.
- Para agendamentos de **pacotes**, é obrigatório informar:
  - `CodProcedimento`
  - `TUSS`
  - `CodigoVenda`

---

## Headers

| Header | Valor |
|----------|------------|
| Authorization | Bearer {token} |

### Exemplo

```
Authorization: Bearer TokenObtidoAnteriormente
```

---

## Body da Requisição

```json
{
  "CodUnidade": 1,
  "CodEspecialidade": 1,
  "CodPlano": 1,
  "NumCarteirinha": "1",
  "CodHorario": 1,
  "Data": "2020-09-28T08:00:00",
  "CodUsuario": 1,
  "CodColaborador": 1,
  "CodProcedimento": 1,
  "BitTelemedicina": true,
  "Confirmada": true,
  "TUSS": "123",
  "CodigoVenda": 1
}
```

---

## Parâmetros do Body

| Campo | Tipo | Obrigatório | Descrição |
|----------|------------|----------------|----------------|
| CodUnidade | int | Sim | Código da unidade |
| CodEspecialidade | int | Sim | Código da especialidade |
| CodPlano | int | Sim | Código do plano |
| NumCarteirinha | string | Não | Número da carteirinha do convênio |
| CodHorario | int | Sim | Código do horário disponível |
| Data | datetime | Não | Data e hora do agendamento. Utilizado apenas quando `CodHorario = 0` |
| CodUsuario | int | Sim | Código do paciente |
| CodColaborador | int | Sim | Código do colaborador |
| CodProcedimento | int | Não | Código do procedimento |
| BitTelemedicina | bool | Sim | Indica se o atendimento será por telemedicina |
| Confirmada | bool | Não | Permite confirmar automaticamente o agendamento |
| TUSS | string | Não | Código TUSS do procedimento (utilizado em pacotes) |
| CodigoVenda | int | Não | Código da venda do pacote |

---

## Response 200 - Sucesso

```json
{
  "Message": "Consulta confirmada com sucesso!",
  "CodAgendamento": 123,
  "CodHorario": 123
}
```

---

## Response 404 - Erro

```json
{
  "message": "Não foi possível confirmar o agendamento."
}
```
