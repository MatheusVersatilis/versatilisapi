# Dados do Usuário por Código

Retorna os dados cadastrais do usuário com base no código informado.

---

## Endpoint

`GET /api/Login/DadosUsuarioPorCodigo`

---

## Query Parameters

| Parâmetro   | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| CodUsuario | integer | Sim        | Código do usuário |

---

## Exemplo de Requisição

```
GET /api/Login/DadosUsuarioPorCodigo?CodUsuario=1
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
  "CodUsuario": "1",
  "Nome": "Teste",
  "CPF": "111.111.111-11",
  "Email": "teste@teste.com.br",
  "Senha": "123456",
  "DtNasc": "10/08/2017",
  "Sexo": "M",
  "Telefone": "1122322112",
  "Celular": "11922123324",
  "CEP": "08635709",
  "Endereco": "Rua de Teste",
  "Numero": "12",
  "Complemento": "Teste",
  "Bairro": "Teste",
  "Cidade": "SUZANO",
  "FacebookID": " "
}
```

---

## Response 404 - Não encontrado

```json
{
  "Usuário não encontrado."
}
```

---

## Observações

- O código do usuário deve existir na base de dados.
- O retorno contém os dados cadastrais atualmente registrados.
