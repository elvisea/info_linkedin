# Experiência profissional

Backup manual do LinkedIn. **Cada cargo** é uma pasta `experience/{id}/` com **`pt-br.md`** e **`en-us.md`**.

**Convenção de `id`:** slug em minúsculas com hífens (ex.: `sh-squads`, `spro-it-solutions`).

## Índice

| Empresa                  | Português                               | English                                 |
| ------------------------ | --------------------------------------- | --------------------------------------- |
| Trio                     | [pt-br.md](trio/pt-br.md)               | [en-us.md](trio/en-us.md)               |
| SH Squads                | [pt-br.md](sh-squads/pt-br.md)          | [en-us.md](sh-squads/en-us.md)          |
| Contabilizei             | [pt-br.md](contabilizei/pt-br.md)       | [en-us.md](contabilizei/en-us.md)       |
| b2k Technology Solutions | [pt-br.md](b2k/pt-br.md)                | [en-us.md](b2k/en-us.md)                |
| SPRO IT Solutions        | [pt-br.md](spro-it-solutions/pt-br.md)  | [en-us.md](spro-it-solutions/en-us.md)  |
| ztrax                    | [pt-br.md](ztrax/pt-br.md)              | [en-us.md](ztrax/en-us.md)              |
| MobileSys Sistemas       | [pt-br.md](mobilesys-sistemas/pt-br.md) | [en-us.md](mobilesys-sistemas/en-us.md) |

_(Adicione nova pasta `{id}/` e linhas na tabela ao incluir uma experiência.)_

---

## Apêndice: tentativa MCP (`get_person_profile`)

**Username:** `elvisea` · **Data:** 2026-04-09

Resposta com listas vazias:

```json
{
  "name": null,
  "about": [],
  "experiences": [],
  "educations": [],
  "interests": [],
  "accomplishments": [],
  "contacts": [],
  "company": null,
  "job_title": null,
  "open_to_work": false
}
```

**Possíveis causas:** HTML/limitações do LinkedIn, scraper, sessão ou migração do MCP para Patchright + `~/.linkedin-mcp/`.

**Referência:** [stickerdaniel/linkedin-mcp-server](https://github.com/stickerdaniel/linkedin-mcp-server)
