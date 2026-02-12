# Excluir Todas Notificações

Exclui todas as notificações do usuário informado.  
Após a exclusão, nenhuma notificação será retornada pelo endpoint de listagem.

---

## Endpoint

`DELETE /api/Notificacao/ExcluirTodasNotificacoes`

---

## Query Parameters

| Parâmetro   | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| CodUsuario | integer | Sim        | Código do usuário |

---

## Exemplo de Requisição

```
DELETE /api/Notificacao/ExcluirTodasNotificacoes?CodUsuario=6014
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

Retornado quando todas as notificações forem excluídas com sucesso.

---

## Response 500 - Erro interno

Retornado quando ocorre erro inesperado no servidor.
