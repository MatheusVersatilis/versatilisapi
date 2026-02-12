# Listar Especialidades com Agenda

Retorna as especialidades que possuem agenda aberta.  
Caso o parâmetro `nomeEspecialidade` esteja vazio, todas as especialidades com agenda disponível serão listadas.

Se `dataSelecionada` for informada, o retorno será filtrado para exibir apenas especialidades com agenda disponível na data especificada.

---

## Endpoint

`GET /api/Especialidade/EspecialidadesAgenda`

---

## Query Parameters

| Parâmetro         | Tipo     | Obrigatório | Padrão | Descrição |
|-------------------|----------|------------|--------|------------|
| nomeEspecialidade | string   | Não        | —      | Nome (ou parte do nome) da especialidade |
| codConvenio       | int      | Não        | —      | Código do convênio para filtro |
| codPlano          | int      | Não        | —      | Código do plano para filtro |
| filtrarPortal     | boolean  | Não        | true   | Quando `true`, retorna apenas especialidades disponíveis no portal |
| dataSelecionada   | datetime | Não        | —      | Data específica para verificar disponibilidade de agenda (formato: YYYY-MM-DD) |

---

## Exemplo de Requisição

```
GET /api/Especialidade/EspecialidadesAgenda?nomeEspecialidade=teste&codConvenio=7&codPlano=7&filtrarPortal=true&dataSelecionada=2026-01-19
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
    "CodEspecialidade": 5,
    "NomeEspecialidade": "CARDIOLOGIA",
    "Preco": 0.0,
    "Descricao": "<p>CARDIOLOGIA TRATA AS DOEN&Ccedil;AS CARDIOVASCULARES</p>\n"
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
