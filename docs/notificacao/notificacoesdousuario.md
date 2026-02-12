# Listar Notificações do Usuário

Retorna todas as notificações disponíveis para o usuário informado, exceto aquelas que já foram excluídas ou vencidas.

---

## Endpoint

`GET /api/Notificacao/Notificacoes`

---

## Query Parameters

| Parâmetro   | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| CodUsuario | integer | Sim        | Código do usuário |

---

## Exemplo de Requisição

```
GET /api/Notificacao/Notificacoes?CodUsuario=6026
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
    "CodigoNotificacao": "C_36461",
    "Texto": "AGENDAMENTO CARDIOLOGIA - ELETROCARDIOGRAMA AMANHÃ ÀS 08:00",
    "DataEvento": "2025-10-22T08:00:00"
  }
]
```

---

## Response 204 - Sem conteúdo

Retornado quando o usuário não possui notificações disponíveis.

---

## Response 500 - Erro interno

Retornado quando ocorre erro inesperado no servidor.
