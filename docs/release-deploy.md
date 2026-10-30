# Release Pipeline Classic e deploy

| Campo | Valor | Estado |
|---|---|---|
| Release Pipeline | `New release pipeline` | Confirmado |
| Stage | `Deploy-Producao` | Confirmado |
| Artifact de origem | Build `CP03-Azure-DevOps-CI`, artifact `drop` | Confirmado |
| Alias do Artifact | A verificar | |
| Continuous Deployment trigger | Habilitado para `main` | Confirmado pelo autor |
| Service Connection | `sc-cp03-azure` | Confirmado |
| App Service | `app-cp03-prisma` (Linux) | Confirmado |
| Task de deploy e pacote/pasta usados | A verificar | |
| Comando de inicialização | A verificar (o `package.json` usa `npm start`) | |
| Release-1 | Stage `Deploy-Producao` executado com sucesso | Confirmado pelo autor; print pendente |
| Release-2 | Continuous deployment, artifact da Build #2, branch `main`; `Deploy-Producao` **Succeeded** em 30/10/2026, 12:16 | Confirmado: [print](../entregaveis/evidencias/06-release-deploy/release-2-succeeded.png); ver [teste-automacao.md](teste-automacao.md) |
| Task de deploy | `Deploy Azure App Service` (nome visível no log da Release-2) | Parâmetros a verificar |

## Critérios de sucesso

1. Release com o stage `Deploy-Producao` em Succeeded.
2. Aplicação abrindo em <https://app-cp03-prisma-e6enhqhrfffch2f4.brazilsouth-01.azurewebsites.net/>.
3. Em um novo deploy, o conteúdo da página reflete o código enviado.

Evidência: [06-release-deploy](../entregaveis/evidencias/06-release-deploy/) e [07-aplicacao-publicada](../entregaveis/evidencias/07-aplicacao-publicada/).
