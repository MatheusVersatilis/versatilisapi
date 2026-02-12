# Vender Pacote

Realiza a venda de um pacote para o paciente.

> ⚠ Este endpoint pode passar por ajustes/mudanças futuras.
> É importante armazenar o `CodigoVenda`, pois ele será utilizado posteriormente (ex: agendamento de sessões do pacote) ou poderá ser recuperado pelo endpoint **Listar Pacotes Vendidos**.

---

## Endpoint

`POST /api/Pacote/VenderPacote`

---

## Headers

| Header        | Valor |
|---------------|--------|
| Authorization | Bearer {token} |
| Content-Type  | application/json |

### Exemplo

```
Authorization: Bearer TokenObtidoAnteriormente
```

---

## Body (JSON)

```json
{
  "CodUsuario": 3011,
  "CodPlano": 6,
  "CodPacote": 1002,
  "NumCarteirinha": "123456789"
}
```

---

## Schema

```json
{
  "type": "object",
  "required": true,
  "additionalProperties": false,
  "properties": {
    "CodUsuario": {
      "type": "int",
      "required": true,
      "description": "Código do paciente."
    },
    "CodPlano": {
      "type": "int",
      "required": true,
      "description": "Código do plano de convênio do paciente."
    },
    "CodPacote": {
      "type": "int",
      "required": true,
      "description": "Código do pacote para a venda."
    },
    "NumCarteirinha": {
      "type": "string",
      "required": false,
      "description": "Número de carteirinha para salvar no convênio."
    }
  }
}
```

---

## Response 200 - Sucesso

> Caso a data de vencimento seja igual ao dia atual, o pacote não possui vencimento configurado.

```json
{
  "Message": "Pacote foi vendido!",
  "CodigoVenda": 9045,
  "Titulos": [
    {
      "CodTitulo": 44467,
      "Valor": 1000.00,
      "DataVencimento": "2025-07-29T00:00:00"
    }
  ]
}
```
