# Aceitar / Confirmar Agendamento

Realiza a aceitação/confirmação de um agendamento previamente realizado.

---

## Endpoint

`PUT /api/Agendamento/ConfirmarAgendamento`

---

## Query Parameters

| Parâmetro       | Tipo    | Obrigatório | Descrição |
|----------------|---------|------------|------------|
| codAgendamento | integer | Sim        | Código do agendamento |

---

## Exemplo de Requisição

```
PUT /api/Agendamento/ConfirmarAgendamento?codAgendamento=36456
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
  "message": "Agendamento confirmado."
}
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Agendamento não encontrado."
}
```
