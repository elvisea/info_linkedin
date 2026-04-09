# Perfil profissional — índice (`knowledge-base/`)

Raiz dos dados versionados: pasta **`knowledge-base/`** (origem: backup LinkedIn). Estrutura tipo **base de conhecimento**: pastas = tipos de entidade; arquivos = registros. Use [`manifest.yaml`](manifest.yaml) para listagem programática (ex.: MCP). Convenções em [`schema/entities.md`](schema/entities.md).

## Perfil (documentos únicos)

| Documento                        | Caminho                                                    |
| -------------------------------- | ---------------------------------------------------------- |
| Informações básicas              | [profile/identity.md](profile/identity.md)                 |
| Sobre                            | [profile/about.md](profile/about.md)                       |
| Preferências de vaga             | [profile/job-preferences.md](profile/job-preferences.md)   |
| Serviços                         | [profile/services.md](profile/services.md)                 |
| Competências em destaque (Sobre) | [profile/skills-highlight.md](profile/skills-highlight.md) |
| Competências (lista completa)    | [profile/skills.md](profile/skills.md)                     |

## Coleções indexadas

| Tipo         | Índice                                              | Conteúdo                                |
| ------------ | --------------------------------------------------- | --------------------------------------- |
| Experiência  | [experience/\_index.md](experience/_index.md)       | `experience/{id}/pt-br.md` · `en-us.md` |
| Formação     | [education/\_index.md](education/_index.md)         | `education/{id}/pt-br.md` · `en-us.md`  |
| Certificados | [certification/\_index.md](certification/_index.md) | `certification/{slug}.md`               |
| Projetos     | [project/\_index.md](project/_index.md)             | `project/{slug}.md`                     |

## Metadados do repositório

| Artefato                                   | Uso                                           |
| ------------------------------------------ | --------------------------------------------- |
| [`manifest.yaml`](manifest.yaml)           | `id`, `type`, caminhos e locales por entidade |
| [`schema/entities.md`](schema/entities.md) | Modelo mental, slugs, relacionamentos         |

---

_Última reorganização estrutural: alinhada ao layout “database-like” (pastas em inglês, conteúdo PT/EN nos arquivos)._
