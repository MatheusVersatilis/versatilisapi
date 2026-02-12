## Cadastrar Novo Usuário
`POST /api/Login/CadastrarUsuario`

Este endpoint é responsável por realizar o cadastro de um novo paciente.

---

## Headers

| Nome | Obrigatório | Descrição |
|-----|------------|-----------|
| Authorization | Sim | Bearer Token obtido anteriormente |

---

## Request Body

```json
{
  "Nome": "Teste",
  "CPF": "111.111.111-11",
  "Email": "teste@teste.com.br",
  "Senha": "e10adc3949ba59abbe56e057f20f883e",
  "DtNasc": "2017-01-12",
  "Sexo": "M",
  "Telefone": "1122322112",
  "Celular": "11922123324",
  "CEP": "08635709",
  "Endereco": "Rua de Teste",
  "Numero": "12",
  "Complemento": "Teste",
  "Bairro": "Teste",
  "Cidade": "SUZANO",
  "FacebookID": "",
  "SemanasGestacao": 1,
  "DiasGestacao": 1,
  "DtParto": "2023-02-10",
  "CodPlano": 1,
  "NumCarteirinha": "123",
  "CodPlanos": [1,2,3,4]
}
```

### Request Schema

| Campo            | Tipo     | Obrigatório | Descrição |
|------------------|----------|-------------|-----------|
| Nome             | string   | Sim         | Nome do usuário |
| CPF              | string   | Sim         | CPF do usuário |
| Email            | string   | Sim         | Email usado no login |
| Senha            | string   | Sim         | Senha em MD5 |
| DtNasc           | string   | Sim         | Data de nascimento (yyyy-MM-dd) |
| Sexo             | string   | Não         | Gênero do usuário |
| Telefone         | string   | Não         | Telefone fixo |
| Celular          | string   | Não         | Celular |
| CEP              | string   | Não         | CEP do endereço |
| Endereco         | string   | Não         | Logradouro |
| Numero           | string   | Não         | Número |
| Complemento      | string   | Não         | Complemento |
| Bairro           | string   | Não         | Bairro |
| Cidade           | string   | Não         | Cidade |
| FacebookID       | string   | Não         | ID do Facebook |
| SemanasGestacao  | integer  | Não         | Semanas de gestação |
| DiasGestacao     | integer  | Não         | Dias de gestação |
| DtParto          | string   | Não         | Data do parto |
| CodPlanos        | array    | Não         | Lista de códigos de plano |


## Response 200
```json
{
    "CodUsuario": "1",
    "Nome": "Teste",
    "CPF": "111.111.111-11",
    "Email": "teste@teste.com.br",
    "Senha": "e10adc3949ba59abbe56e057f20f883e",
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
    "SemanasGestacao": "1",
    "DiasGestacao": "1",
	"DtParto": "2023-02-10"
}
```

## Response 400
```json
{
	"Não foi possivel inserir o usuario"  
}
```