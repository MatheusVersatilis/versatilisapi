# Listar Convênios do Usuário

Retorna os convênios disponíveis para o usuário no portal, de acordo com a unidade e especialidade selecionadas.

---

## Endpoint

`GET /api/Convenio/Planos`

---

## Query Parameters

| Parâmetro         | Tipo | Obrigatório | Descrição |
|------------------|------|------------|------------|
| codUnidade       | int  | Não        | Código da unidade para filtro |
| codEspecialidade | int  | Não        | Código da especialidade para filtro |
| codUsuario       | int  | Sim        | Código do usuário |

---

## Exemplo de Requisição

```
GET /api/Convenio/Planos?codUnidade=1&codEspecialidade=1&codUsuario=1
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
    "CodPlano": 7,
    "NomeConvenio": "CIRAST",
    "NomePlano": "CIRAST/SSP",
    "Ativo": true
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados convênios disponíveis."
}
```
