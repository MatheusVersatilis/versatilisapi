# Listar Dias Disponíveis

Retorna os dias que possuem horários disponíveis de acordo com os filtros informados.

---

## Endpoint

`GET /api/Agenda/DiasDisponiveis`

---

## Query Parameters

| Parâmetro           | Tipo    | Obrigatório | Descrição |
|--------------------|---------|------------|------------|
| codUnidade         | int     | Não        | Código da unidade |
| codEspecialidade   | int     | Sim        | Código da especialidade |
| codPlano           | int     | Sim        | Código do plano |
| codUsuario         | int     | Não        | Código do usuário |
| bitTrazerRetorno   | boolean | Não        | Padrão: `false`. Quando `false` e `codUsuario` for informado, não retorna horários classificados como retorno |

---

## Exemplo de Requisição

```
GET /api/Agenda/DiasDisponiveis?codUnidade=1&codEspecialidade=1&codPlano=1&codUsuario=1&bitTrazerRetorno=true
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
    "Data": "1900-01-01"
  },
  {
    "Data": "1900-01-02"
  }
]
```

> Recomenda-se que o formato da data siga o padrão ISO 8601 (`yyyy-MM-dd`).

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontrados dias disponíveis."
}
```
