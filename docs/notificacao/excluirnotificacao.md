# Excluir Notificação

Exclui uma notificação específica do usuário.  
Após a exclusão, a notificação não será mais retornada no endpoint de listagem.

---

## Endpoint

`DELETE /api/Notificacao/ExcluirNotificacao`

---

## Query Parameters

| Parâmetro           | Tipo   | Obrigatório | Descrição |
|---------------------|--------|------------|------------|
| CodigoNotificacao   | string | Sim        | Código da notificação |

---

## Exemplo de Requisição

```
DELETE /api/Notificacao/ExcluirNotificacao?CodigoNotificacao=C_36461
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
  "Notificação excluída com sucesso."
}
```

---

## Response 500 - Erro interno

Retornado quando ocorre erro inesperado no servidor.
