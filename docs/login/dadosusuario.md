# Dados do Usuário

Retorna os dados do usuário com base nos parâmetros informados no corpo da requisição.  
Todos os campos são opcionais e podem ser utilizados como filtros.

---

## Endpoint

`GET /api/Login/DadosUsuario`

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

## Body (application/json)

Todos os campos são opcionais.

```json
{
  "Nome": "Teste",
  "DtNasc": "2020-01-01 00:00:00",
  "Telefone": "(11)11111-1111",
  "Celular": null,
  "NumCarteirinha": "123"
}
```

---

## Campos Disponíveis para Filtro

| Campo           | Tipo     | Descrição |
|----------------|----------|------------|
| Nome           | string   | Nome do usuário |
| DtNasc         | datetime | Data de nascimento |
| Telefone       | string   | Telefone do usuário |
| Celular        | string   | Celular do usuário |
| NumCarteirinha | string   | Número da carteirinha |

---

## Response 200 - Sucesso

```json
[
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
    "FacebookID": " ",
    "CodPlanos": [1]
  }
]
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

- Todos os campos do body são opcionais.
- A busca pode retornar múltiplos usuários.
- Os planos vinculados ao usuário são retornados no campo `CodPlanos`.
