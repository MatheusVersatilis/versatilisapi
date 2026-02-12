# Listar Procedimentos com Agenda

Retorna os procedimentos que possuem agenda disponível.

Caso o parâmetro `nomeProcedimento` esteja vazio, todos os procedimentos com agenda cadastrados no sistema serão listados.

Se `dataSelecionada` for informada, o retorno será filtrado para exibir apenas procedimentos com disponibilidade na data especificada.

---

## Endpoint

`GET /api/Procedimento/ProcedimentosAgenda`

---

## Query Parameters

| Parâmetro         | Tipo     | Obrigatório | Padrão | Descrição |
|------------------|----------|------------|--------|------------|
| nomeProcedimento | string   | Não        | —      | Nome (ou parte do nome) do procedimento |
| codPlano         | int      | Não        | —      | Código do plano para filtro |
| filtrarPortal    | boolean  | Não        | true   | Quando `true`, retorna apenas procedimentos disponíveis no portal |
| dataSelecionada  | datetime | Não        | —      | Data específica para verificar disponibilidade (formato: YYYY-MM-DD) |

---

## Exemplo de Requisição

```
GET /api/Procedimento/ProcedimentosAgenda?nomeProcedimento=teste&codPlano=7&filtrarPortal=true&dataSelecionada=2026-01-19
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
    "CodProcedimento": 1,
    "NomeProcedimento": "Teste",
    "CodEspecialidade": 2,
    "NomeEsp
