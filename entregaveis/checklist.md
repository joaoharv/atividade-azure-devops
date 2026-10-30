# Checklist de entrega

Classificações: **CONCLUÍDO**, **PENDENTE** e **A VERIFICAR**. Um item só é CONCLUÍDO com link ou imagem que comprove o requisito. Todas as imagens foram abertas e avaliadas.

## Links

| # | Item | Status | Link / evidência | Observações |
|---|---|---|---|---|
| 1 | Repositório GitHub | CONCLUÍDO | <https://github.com/joaoharv/atividade-azure-devops> | Branch `main` |
| 2 | Projeto Azure DevOps | CONCLUÍDO | <https://dev.azure.com/RM564212/CP03-Azure-DevOps> | |
| 3 | Build Pipeline | A VERIFICAR | [links.md](links.md) | Lista de pipelines: <https://dev.azure.com/RM564212/CP03-Azure-DevOps/_build>. Falta o link direto da `CP03-Azure-DevOps-CI` |
| 4 | Azure App Service no Portal | PENDENTE | [links.md](links.md) | Falta a URL do recurso `app-cp03-prisma` no Portal |
| 5 | URL pública da aplicação | CONCLUÍDO | <https://app-cp03-prisma-e6enhqhrfffch2f4.brazilsouth-01.azurewebsites.net/> | Site no ar |

## Evidências (prints)

| # | Item | Status | Arquivo | Avaliação |
|---|---|---|---|---|
| 6 | Pipeline no Editor Clássico | PENDENTE | [lista-pipelines-build-2.png](evidencias/01-pipeline-classic/lista-pipelines-build-2.png) | Mostra a lista de Pipelines com `CP03-Azure-DevOps-CI`. **Não** mostra o Editor Clássico |
| 7 | Tasks configuradas | A VERIFICAR | [build-2-jobs-e-etapas.png](evidencias/03-build/build-2-jobs-e-etapas.png) | Mostra as etapas executadas, com nomes truncados; não é a tela de configuração |
| 8 | Execução da Build | CONCLUÍDO | [build-2-lista-pipelines.png](evidencias/03-build/build-2-lista-pipelines.png), [build-2-jobs-e-etapas.png](evidencias/03-build/build-2-jobs-e-etapas.png) | Build #2 Succeeded, motivo Individual CI. Não há print da Build #1 |
| 9 | Artifact publicado | PENDENTE | — | Nenhuma imagem mostra o Artifact `drop`. Indícios indiretos: "1 artifact produced" no log da Build #2 e o artifact `_CP03-Azure-Dev…` (versão 2) no print da Release-2 |
| 10 | Service Connection | PENDENTE | [05-service-connection](evidencias/05-service-connection/) | Sem imagem; sem expor segredos |
| 11 | Release / Deploy | CONCLUÍDO | [release-2-succeeded.png](evidencias/06-release-deploy/release-2-succeeded.png) | Release-2, Continuous deployment, artifact da Build #2, branch `main`, `Deploy-Producao` Succeeded (30/10/2026, 12:16). Não há print da Release-1 |
| 12 | Aplicação publicada | CONCLUÍDO | [app-badge-antigo.png](evidencias/07-aplicacao-publicada/app-badge-antigo.png) | Site no ar com o badge antigo (primeiro deploy). Falta print com o badge novo |
| 13 | Professor com acesso Basic | PENDENTE | [usuarios-basic.png](evidencias/08-professor-basic/usuarios-basic.png) | O print mostra apenas `profkarlos.lima@fiap.com.br` como Basic. **`pf2488@fiap.com.br` não aparece**; não pode ser declarado como cadastrado |

## Evidência complementar: push e acionamento automático

| Etapa | Status | Evidência | Observações |
|---|---|---|---|
| Build #1 (manual) | CONCLUÍDO | Informado pelo autor | Sem print |
| Release-1, `Deploy-Producao` | CONCLUÍDO | Informado pelo autor | Sem print |
| Commit `69b3be7` enviado à `main` | CONCLUÍDO | Histórico do GitHub | |
| Build #2 por push (Individual CI), Succeeded | CONCLUÍDO | [lista](evidencias/03-build/build-2-lista-pipelines.png), [etapas](evidencias/03-build/build-2-jobs-e-etapas.png) | |
| Release-2 criada por Continuous deployment | CONCLUÍDO | [release-2-succeeded.png](evidencias/06-release-deploy/release-2-succeeded.png), [em andamento](evidencias/09-automacao-git-push/release-2-download-artifact-em-andamento.png) | |
| Release-2 `Deploy-Producao` Succeeded | CONCLUÍDO | [release-2-succeeded.png](evidencias/06-release-deploy/release-2-succeeded.png) | |
| Novo badge no site | A VERIFICAR | Consulta HTTP em 30/10/2026 12:19 devolveu "Deploy realizado com sucesso pelo Azure DevOps!" | Falta o **print** do site com o badge novo em `09-automacao-git-push/` |

## Resumo

- CONCLUÍDO: itens 1, 2, 5, 8, 11 e 12.
- A VERIFICAR: itens 3 e 7.
- PENDENTE: itens 4, 6, 9, 10 e 13.
