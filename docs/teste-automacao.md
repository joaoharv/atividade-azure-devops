# Teste de automação (push → Build → Release)

**Resultado:** o push disparou a Build #2 automaticamente (Individual CI, Succeeded), e a Release-2 foi criada por Continuous deployment e terminou com `Deploy-Producao` em Succeeded. Uma consulta HTTP ao site mostrou o novo badge; falta o print dessa página.

## Alteração testada

Arquivo `app/index.js`, badge da página inicial:

| Antes | Depois |
|---|---|
| `Deploy Status: Sucesso! ✅` | `Deploy realizado com sucesso pelo Azure DevOps!` |

## Deploys

| | Release | Origem | Resultado |
|---|---|---|---|
| **Deploy inicial** | Release-1, `Deploy-Producao` | Build #1, manual | Succeeded (informado pelo autor; sem print) |
| **Segundo deploy** | Release-2, `Deploy-Producao` | Continuous deployment, Build #2, branch `main` | **Succeeded** em 30/10/2026, 12:16 |

## Linha do tempo

| # | Evento | Estado | Evidência |
|---|---|---|---|
| 1 | Build #1 executada manualmente | Succeeded (informado pelo autor) | — |
| 2 | Release-1 criada e executada | Succeeded (informado pelo autor) | — |
| 3 | Site publicado com o badge antigo | Confirmado | [app-badge-antigo.png](../entregaveis/evidencias/07-aplicacao-publicada/app-badge-antigo.png) |
| 4 | Commit `69b3be7` e push na `main` | Confirmado | Histórico do GitHub |
| 5 | Build #2 iniciada automaticamente, motivo Individual CI | Confirmado | [lista-pipelines-build-2.png](../entregaveis/evidencias/01-pipeline-classic/lista-pipelines-build-2.png) |
| 6 | Build #2 concluída, Succeeded (cerca de 37 min) | Confirmado | [build-2-lista-pipelines.png](../entregaveis/evidencias/03-build/build-2-lista-pipelines.png), [build-2-jobs-e-etapas.png](../entregaveis/evidencias/03-build/build-2-jobs-e-etapas.png) |
| 7 | Release-2 em execução (`Download artifact` do `drop`) | Confirmado | [release-2-download-artifact-em-andamento.png](../entregaveis/evidencias/09-automacao-git-push/release-2-download-artifact-em-andamento.png) |
| 8 | Release-2: Continuous deployment, artifact da Build #2 (versão 2), `main`, `Deploy-Producao` Succeeded | Confirmado | [release-2-succeeded.png](../entregaveis/evidencias/06-release-deploy/release-2-succeeded.png) |
| 9 | Site com o novo badge | Confirmado por consulta HTTP em 30/10/2026, 12:19 (HTTP 200); **sem print** | Pendente: print em `09-automacao-git-push/` |

## Observação

O download do artifact na Release-2 lista arquivos de `node_modules`, e a publicação do Artifact na Build #2 levou cerca de 36 min. Ver [artifact.md](artifact.md).
