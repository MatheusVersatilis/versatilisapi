# Solicitar Nova Senha

Realiza a solicitação de uma nova senha para o usuário.  
A nova senha será enviada para o e-mail cadastrado.

---

## Endpoint

`GET /api/Login/SolicitarSenha`

---

## Query Parameters

| Parâmetro       | Tipo     | Obrigatório | Descrição |
|----------------|----------|------------|------------|
| login          | string   | Sim        | Login do usuário (e-mail, código do usuário ou CPF) |
| dtNasc         | datetime | Sim        | Data de nascimento do usuário |

---

## Exemplo de Requisição

```
GET /api/Login/SolicitarSenha?login=UsuarioTeste&dtNasc=10/08/2017
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
  "Senha enviado por e-mail ao cliente."
}
```

---

## Response 404 - Não encontrado

```json
{
  "Usuário não encontrado."
}
```
