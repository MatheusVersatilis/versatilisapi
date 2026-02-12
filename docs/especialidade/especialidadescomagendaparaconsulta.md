# Listar Especialidades com Agenda para Consulta

Retorna as especialidades que possuem agenda disponível para consulta.

Caso o parâmetro `nomeEspecialidade` esteja vazio, todas as especialidades com agenda para consulta serão listadas.

---

## Endpoint

`GET /api/Especialidade/EspecialidadesAgendaConsulta`

---

## Query Parameters

| Parâmetro         | Tipo    | Obrigatório | Padrão | Descrição |
|-------------------|---------|------------|--------|------------|
| nomeEspecialidade | string  | Não        | —      | Nome (ou parte do nome) da especialidade |
| codPlano          | int     | Não        | —      | Código do plano para filtro |
| filtrarPortal     | boolean | Não        | true   | Quando `true`, retorna apenas especialidades disponíveis no portal |

---

## Exemplo de Requisição

```
GET /api/Especialidade/EspecialidadesAgendaConsulta?nomeEspecialidade=teste&codPlano=7&filtrarPortal=true
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
    "CodEspecialidade": 1,
    "NomeEspecialidade": "CLINICO GERAL",
    "Descricao": "CLINICO GERAL TRATA AS DOENÇAS GERAIS"
  }
]
```

---

## Response 404 - Não encontrado

```json
{
  "message": "Não foram encontradas especialidades cadastradas."
}
```
