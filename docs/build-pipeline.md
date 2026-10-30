# Build Pipeline Classic

| Campo | Valor | Estado |
|---|---|---|
| Nome | `CP03-Azure-DevOps-CI` | Confirmado |
| Editor | Classic | Confirmado |
| Origem | GitHub `joaoharv/atividade-azure-devops` | Confirmado |
| Branch | `main` | Confirmado |
| Execução | Concluída com sucesso, Artifact `drop` publicado | Confirmado pelo autor; print pendente |
| Agent pool / SO do agente | A verificar |  |
| Gatilho de CI (Enable continuous integration) | A verificar |  |
| Versão do Node.js configurada | A verificar |  |

## Tasks

Os nomes, ordem e parâmetros das tasks **não foram registrados aqui** porque dependem de conferência na interface (Pipelines → `CP03-Azure-DevOps-CI` → Edit). Preencher a tabela depois de abrir a pipeline:

| # | Finalidade esperada | Task / comando | Estado |
|---|---|---|---|
| 1 | Configurar Node.js | A verificar | A verificar |
| 2 | Instalar dependências (`npm install` em `app/`) | A verificar | A verificar |
| 3 | Validar a aplicação | A verificar | A verificar |
| 4 | Copiar arquivos de publicação | A verificar | A verificar |
| 5 | Publicar o Artifact `drop` | A verificar | A verificar |

O projeto só tem o script `npm start`; não existem `build` nem `test`. Evidência: [entregaveis/evidencias/02-tasks](../entregaveis/evidencias/02-tasks/) e [03-build](../entregaveis/evidencias/03-build/).
