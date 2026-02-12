# Confirmar Agendamento

Confirma um agendamento existente.

Equivalente ao botão **"Confirmar"** na Ficha do Paciente.  
Ao confirmar por este método, o profissional da saúde é liberado para realizar o atendimento e o agendamento passa para o status **Confirmado**.

---

## Endpoint

`PUT /api/Agenda/PutAgendamento`

---

## Query Parameters

| Parâmetro       | Tipo | Obrigatório | Descrição |
|----------------|------|------------|------------|
| codAgendamento | int  | Sim        | Código do agendamento |

---

## Exemplo de Requisição

```
PUT /api/Agenda/PutAgendamento?codAgendamento=1
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
  "Message": "Agendamento confirmado com sucesso!"
}
```

---

## Response 400 - Erro de Regra

```json
{
  "Message": "Não foi possível confirmar o agendamento. Motivo: ..."
}
```

---

## Response 404 - Não encontrado

```json
{
  "Message": "Agendamento não encontrado!"
}
```
