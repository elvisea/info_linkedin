# Plano de ação — export LinkedIn (`linkedin-export-2026-04-09.zip`)

Objetivo: lembrar o que há dentro do ZIP, como usar com o [knowledge-base/](../knowledge-base/), o que diverge do backup manual e o que melhorar a seguir.

## Como voltar aos dados

- Arquivo local: **`linkedin-export-2026-04-09.zip`** (raiz deste repositório, se o mantiveres aqui).
- Extrair para uma pasta **temporária** (ex.: `tmp/linkedin-export/`, não versionada) e trabalhar a partir dos CSV.

## Mapa rápido CSV → knowledge-base

| CSV no export                     | Uso no KB                                                                                      |
| --------------------------------- | ---------------------------------------------------------------------------------------------- |
| `Profile.csv`                     | Cruzar headline, summary e websites com `knowledge-base/profile/about.md` e `identity.md`      |
| `Positions.csv`                   | Textos longos de descrição → `knowledge-base/experience/*/en-us.md` (e PT se quiseres)         |
| `Education.csv`                   | Validar com `knowledge-base/education/*`                                                       |
| `Certifications.csv`              | URLs e códigos → `knowledge-base/certification/*.md` (alto impacto onde o backup estava vazio) |
| `Skills.csv`                      | Validar com `knowledge-base/profile/skills.md`                                                 |
| `Projects.csv`                    | Validar com `knowledge-base/project/*.md`                                                      |
| `Jobs/Job Seeker Preferences.csv` | Cruzar com `knowledge-base/profile/job-preferences.md`                                         |

## Divergências conhecidas

Corrigir com base na verdade contratual, histórico no LinkedIn ou repositórios dos projetos.

| Tema                                 | Situação                                                                                                                   | Ação sugerida                                                                                                         |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **SH Squads — datas**                | No export (`Positions.csv`) aparece **Mar 2025 – Jun 2025**; no KB (`experience/sh-squads/`) está **Mar 2024 – Jun 2024**. | Confirmar qual está certo; alinhar Markdown (e o LinkedIn, se ainda estiver ativo) antes de confiar só no CSV.        |
| **Go Barber vs Be The Hero**         | O mesmo link `bit.ly/4exyJOF` nos dois projetos no export e no KB.                                                         | Verificar no GitHub/portfolio qual URL é de qual projeto; corrigir no KB.                                             |
| **Fastify**                          | No perfil LinkedIn a competência aparece como **`fastfy`** (typo).                                                         | Corrigir no LinkedIn se possível; no KB podes normalizar para **Fastify** com nota.                                   |
| **Certificados Rocketseat “vazios”** | Vários `.md` em `certification/` ficaram sem URL/código no backup manual.                                                  | O `Certifications.csv` traz URLs (incl. `app.rocketseat.com.br`) e _license number_ — atualizar as tabelas nos `.md`. |

## Arquivo `linkedin-export-2026-04-09.zip` no repositório

- O export está **versionado** na raiz do projeto como ZIP **protegido por senha** (definida por ti).
- Há **cópia adicional no Google Drive** — bom para recuperação fora do Git.
- **Nunca** commits nem documentos no repo com a **senha** do ZIP; guarda-a só no gestor de senhas / nota segura no Drive.
- Mesmo encriptado, o ficheiro no GitHub é **público** se o repositório for público; usa **senha forte** e aceita o risco residual de alguém tentar quebrar o arquivo.

## Dados sensíveis

Não copiar para Markdown público no repositório sem decisão explícita:

- `Profile.csv`: data de nascimento; combinar com ficheiros de email/telefone do export.
- `messages.csv`, `Email Addresses.csv`, `PhoneNumbers.csv`, `Whatsapp Phone Numbers.csv`.
- `Connections.csv`, `Invitations.csv`: dados de terceiros — usar só offline ou de forma agregada.

Ao **extrair** o ZIP localmente, continua a preferir pasta temporária (`tmp/`) para não versionar CSV soltos com PII.

## Melhorias próximas (prioridade sugerida)

1. **Certificados** — sincronizar URL e código a partir de `Certifications.csv` → `knowledge-base/certification/*.md`.
2. **Experiências** — incorporar descrições longas de `Positions.csv` em `experience/*/en-us.md`, **sem mudar datas** até resolver SH Squads.
3. **Perfil e preferências de vaga** — diff entre `Profile.csv` / `Job Seeker Preferences.csv` e `about.md` / `job-preferences.md`.
4. **manifest.yaml** — após alterações grandes no KB, rever títulos e caminhos.
5. **MCP futuro** — ler `manifest.yaml` + Markdown; opcionalmente um script em `scripts/` que leia CSV e sugira diffs.
6. **Novo export** — ao baixar de novo, renomear com data (`linkedin-export-AAAA-MM-DD.zip`) e repetir esta checklist.
