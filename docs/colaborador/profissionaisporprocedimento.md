# Listar Profissionais por Procedimento

Retorna os profissionais disponíveis para o procedimento informado.

---

## Endpoint

`GET /api/Colaborador/ProfissionalByProcedimento`

---

## Query Parameters

| Parâmetro       | Tipo | Obrigatório | Descrição |
|----------------|------|------------|------------|
| CodProcedimento | int  | Sim        | Código do procedimento |

---

## Exemplo de Requisição

```
GET /api/Colaborador/ProfissionalByProcedimento?CodProcedimento=1
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
    "CodColaborador": 1,
    "Nome": "PROFISSIONAL TESTE",
    "Procedimentos": [
      {
        "CodProcedimento": 1,
        "NomeProcedimento": "PROCED EXEMPLO"
      }
    ]
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados profissionais disponíveis para o procedimento informado."
}
```
