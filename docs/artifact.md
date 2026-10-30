# Artifact

- **Nome:** `drop` (confirmado).
- **Origem:** Build `CP03-Azure-DevOps-CI`.
- **Conteúdo observado:** cerca de 17 mil arquivos, incluindo `node_modules`. Um `npm install` local gera 17.211 arquivos e 125 MB em `node_modules`, o que explica a publicação lenta.
- **Estrutura interna e alias na Release:** A verificar.

## Possível otimização (não aplicada)

Publicar apenas `index.js`, `package.json` e `package-lock.json` e deixar o App Service instalar as dependências no deploy (por exemplo com `SCM_DO_BUILD_DURING_DEPLOYMENT`). Isso exige alterar a Build Classic ou configurações do App Service, e não foi feito por restrição da atividade. Se for adotado, validar antes que o site continue funcionando.

Evidência: [04-artifact](../entregaveis/evidencias/04-artifact/).
