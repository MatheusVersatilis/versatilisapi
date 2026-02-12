# Listar Unidades por Especialidade

Retorna as unidades disponíveis no portal para a especialidade informada.

Caso o cliente tenha configurado regiões de unidades no sistema Versatilis, poderá haver mais de uma região retornada.  
Caso contrário, será retornada uma única região com o nome **"UNICA"**.

---

## Endpoint

`GET /api/Unidade/UnidadesPorEspecialidade`

---

## Query Parameters

| Parâmetro        | Tipo | Obrigatório | Descrição |
|------------------|------|------------|------------|
| codEspecialidade | int  | Sim        | Código da especialidade |

---

## Exemplo de Requisição

```
GET /api/Unidade/UnidadesPorEspecialidade?codEspecialidade=1
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

## Response 200 - Sucesso (Sem Regiões Configuradas)

```json
[
  {
    "CodRegiao": 0,
    "NomeRegiao": "UNICA",
    "Unidades": [
      {
        "CodUnidade": 1,
        "NomeUnidade": "CLÍNICA VERSATILIS"
      }
    ]
  }
]
```

---

## Response 200 - Sucess
