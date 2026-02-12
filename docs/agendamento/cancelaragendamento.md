# Cancelar Agendamento

Realiza o cancelamento de um agendamento previamente realizado.

> O cancelamento é permitido apenas para agendamentos com status "Agendada".

---

## Endpoint

`PUT /api/Agendamento/CancelarAgendamento`

---

## Query Parameters

| Parâmetro       | Tipo    | Obrigatório | Descrição |
|----------------|---------|------------|------------|
| codAgendamento | integer | Sim        | Código do agendamento |
| Motivo         | string  | Sim        | Motivo do cancelamento (ex: `VIA INTEGRAÇÃO`) |

---

## Exemplo de Requisição

```
PUT /api/Agendamento/CancelarAgendamento?codAgendamento=36456&Motivo=VIA%20INTEGRACAO
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
  "message": "Cancelamento realizado com sucesso!!."
}
```

---

## Response 404 - Erro

```json
{
  "message": "Não foi Possivel Cancelar o Agendamento."
}
```
