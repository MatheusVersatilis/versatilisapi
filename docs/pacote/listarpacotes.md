# Listar Pacotes

Retorna os pacotes disponíveis para venda de acordo com o plano informado e, opcionalmente, a unidade.

---

## Endpoint

`GET /api/Pacote/ListarPacotes`

---

## Query Parameters

| Parâmetro  | Tipo    | Obrigatório | Descrição |
|------------|---------|------------|------------|
| CodPlano   | integer | Sim        | Código do plano |
| CodUnidade | integer | Não        | Código da unidade |

---

## Exemplo de Requisição

```
GET /api/Pacote/ListarPacotes?CodPlano=1&CodUnidade=1
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
    "CodPacote": 1002,
    "NomePacote": "PACOTE DE FISIOTERAPIA",
    "QtdDiasValidade": null,
    "ValorParcela": 1000.00,
    "QtdParcelas": 1,
    "Unidade": {
      "CodUnidade": 1,
      "NomeUnidade": "UNIDADE 1",
      "Endereco": "RUA ALTERAR 001  CIDADE BAIXA, 90050-310 - PORTO ALEGRE/RS"
    },
    "Itens": [
      {
        "CodEspecialidade": 4,
        "Especialidade": "FISIOTERAPIA",
        "CodProcedimento": 2004,
        "Procedimento": "SESSÃO DE FISIOTERAPIA",
        "CodMaterial": null,
        "Material": null,
        "QtdSessao": 0
      },
      {
        "CodEspecialidade": 1003,
        "Especialidade": "QUIROPRAXIA",
        "CodProcedimento": 3,
        "Procedimento": "SESSÃO DE QUIROPRAXIA",
        "CodMaterial": null,
        "Material": null,
        "QtdSessao": 0
      },
      {
        "CodEspecialidade": 5,
        "Especialidade": "CARDIOLOGIA",
        "CodProcedimento": 2,
        "Procedimento": "ECOCARDIOGRAMA",
        "CodMaterial": null,
        "Material": null,
        "QtdSessao": 0
      }
    ]
  }
]
```

---

## Response 204 - Sem conteúdo

Retornado quando não há pacotes disponíveis para os parâmetros informados.
