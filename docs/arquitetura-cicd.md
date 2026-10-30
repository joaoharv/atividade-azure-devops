# Arquitetura CI/CD

```mermaid
sequenceDiagram
    actor Dev
    participant GH as GitHub (main)
    participant B as Classic Build CP03-Azure-DevOps-CI
    participant A as Artifact drop
    participant R as Classic Release Deploy-Producao
    participant App as App Service app-cp03-prisma
    Dev->>GH: git push
    GH->>B: gatilho de CI
    B->>A: publica Artifact
    A->>R: gatilho de CD
    R->>App: deploy via sc-cp03-azure
```

## Componentes

| Componente | Valor | Estado |
|---|---|---|
| Repositório | `joaoharv/atividade-azure-devops`, branch `main` | Confirmado |
| Organização / projeto | `RM564212` / `CP03-Azure-DevOps` | Confirmado |
| Build | `CP03-Azure-DevOps-CI` (Classic Editor) | Confirmado |
| Artifact | `drop` | Confirmado |
| Service Connection | `sc-cp03-azure` | Confirmado |
| Release | `New release pipeline`, stage `Deploy-Producao` | Confirmado |
| App Service | `app-cp03-prisma` (Linux), grupo `rg-cp03-devops` | Confirmado |
| Subscription | Azure for Students | Confirmado |

## Decisões

- Pipelines **Classic**, conforme exigido; não há YAML de pipeline neste repositório.
- O workflow do GitHub Actions ficou somente manual para evitar um segundo deploy.
- Nenhum segredo é guardado no Git; a autenticação fica na Service Connection.
