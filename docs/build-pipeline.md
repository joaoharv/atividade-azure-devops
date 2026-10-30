# Build Pipeline Classic

| Campo | Valor | Estado |
|---|---|---|
| Nome | `CP03-Azure-DevOps-CI` | Confirmado |
| Editor | Classic | Confirmado |
| Origem | GitHub `joaoharv/atividade-azure-devops` | Confirmado |
| Branch | `main` | Confirmado |
| Execução | Concluída com sucesso, Artifact `drop` publicado | Confirmado pelo autor; print pendente |
| Agent pool / imagem | Azure Pipelines / `ubuntu-latest` | Confirmado no log da Build #2 |
| Gatilho de CI | A Build #2 foi iniciada por push, motivo Individual CI | Confirmado; configuração exata a verificar |
| Duração da Build #2 | Cerca de 37 min (a etapa de publicar o Artifact levou 36 min 33 s) | Confirmado |
| Versão do Node.js configurada | A verificar |  |

## Tasks

O log da Build #2 mostra estas etapas, com os nomes truncados na captura ([build-2-jobs-e-etapas.png](../entregaveis/evidencias/03-build/build-2-jobs-e-etapas.png)): Checkout, "Verificar ambie…", "Instalar depend…", "Validar aplicaçã…", "Preparar arquivo…" e "Publicar Ar…". Os nomes completos, tipos de task e parâmetros dependem de conferência na interface (Pipelines → `CP03-Azure-DevOps-CI` → Edit). Preencher a tabela depois de abrir a pipeline:

| # | Finalidade esperada | Task / comando | Estado |
|---|---|---|---|
| 1 | Configurar Node.js | A verificar | A verificar |
| 2 | Instalar dependências (`npm install` em `app/`) | A verificar | A verificar |
| 3 | Validar a aplicação | A verificar | A verificar |
| 4 | Copiar arquivos de publicação | A verificar | A verificar |
| 5 | Publicar o Artifact `drop` | A verificar | A verificar |

O projeto só tem o script `npm start`; não existem `build` nem `test`. Evidência: [entregaveis/evidencias/02-tasks](../entregaveis/evidencias/02-tasks/) e [03-build](../entregaveis/evidencias/03-build/).
