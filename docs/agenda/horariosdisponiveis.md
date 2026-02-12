# Listar Horários Disponíveis

Retorna os horários disponíveis para o dia selecionado, de acordo com os filtros informados.

---

## Endpoint

`GET /api/Agenda/HorariosDisponiveis`

---

## Query Parameters

| Parâmetro         | Tipo    | Obrigatório | Descrição |
|------------------|---------|------------|------------|
| codUnidade       | int     | Não        | Código da unidade |
| codEspecialidade | int     | Sim        | Código da especialidade |
| codPlano         | int     | Sim        | Código do plano |
| diaSelecionado   | date    | Sim        | Data desejada no formato `YYYY-MM-DD` |
| codUsuario       | int     | Sim        | Código do usuário |
| codProcedimento  | int     | Não        | Código do procedimento |
| filtrarPortal    | boolean | Não        | Padrão: `true`. Filtra somente especialidades disponíveis no portal |
| bitTrazerRetorno | boolean | Não        | Padrão: `false`. Quando `false` e `codUsuario` for informado, não retorna horários classificados como retorno |

---

## Exemplo de Requisição

```
GET /api/Agenda/HorariosDisponiveis?codUnidade=1&codEspecialidade=1&codPlano=1&diaSelecionado=2017-03-07&codUsuario=1&codProcedimento=1&filtrarPortal=true&bitTrazerRetorno=false
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
    "NomeMedico": "Dr. Teste1",
    "CRM": "105012",
    "Observacao": "TESTE",
    "OrdemChegada": false,
    "Horarios": [
      {
        "CodHorario": 1,
        "Horario": "08:00",
        "CodUnidade": 1,
        "Unidade": "CLINICA VERSATILIS",
        "PermiteConsulta": true,
        "PermiteProcedimento": true,
        "Procedimentos": [
          {
            "CodProcedimento": 1,
            "NomeProcedimento": "TRATAMENTO"
          }
        ]
      }
    ]
  }
]
```

> Observação: Recomenda-se manter padrões consistentes de nomenclatura (ex: evitar acentos em propriedades JSON).

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados horários disponíveis."
}
```
