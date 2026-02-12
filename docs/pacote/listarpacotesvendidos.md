# Listar Pacotes Vendidos

Retorna os pacotes vendidos para o paciente informado.

---

## Endpoint

`GET /api/Pacote/ListarPacotesVendidos`

---

## Query Parameters

| Parâmetro   | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| CodUsuario | integer | Sim        | Código do usuário (paciente) |

---

## Exemplo de Requisição

```
GET /api/Pacote/ListarPacotesVendidos?CodUsuario=3011
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
    "CodigoVenda": 9035,
    "CodPacote": 6018,
    "NomePacote": "PACOTE DE TESTE",
    "ValorTotal": 1200.00,
    "DataValidade": null,
    "Vencido": false,
    "VendidoWeb": false,
    "StatusFinanceiro": "TITULO LIQUIDADO",
    "Unidade": {
      "CodUnidade": 1,
      "NomeUnidade": "UNIDADE 1",
      "Endereco": "RUA TESTE 001  CIDADE BAIXA, 90050-310 - PORTO ALEGRE/RS"
    },
    "Itens": []
  },
  {
    "CodigoVenda": 9038,
    "CodPacote": 6019,
    "NomePacote": "HIDROGINASTICA",
    "ValorTotal": 1000.00,
    "DataValidade": null,
    "Vencido": false,
    "VendidoWeb": false,
    "StatusFinanceiro": "TITULO EM ABERTO",
    "Unidade": {
      "CodUnidade": 1,
      "NomeUnidade": "UNIDADE 1",
      "Endereco": "RUA TESTE 001  CIDADE BAIXA, 90050-310 - PORTO ALEGRE/RS"
    },
    "Itens": [
      {
        "CodEspecialidade": 4,
        "NomeEspecialidade": "FISIOTERAPIA",
        "CodProcedimento": 10018,
        "NomeProcedimento": "HIDROGINASTICA",
        "NumSessoesTotais": 5,
        "NumSessoesRealizadas": 5,
        "NumSessoesRestantes": 0
      }
    ]
  }
]
```

---

## Response 204 - Sem conteúdo

Retornado quando o paciente não possui pacotes vendidos.
