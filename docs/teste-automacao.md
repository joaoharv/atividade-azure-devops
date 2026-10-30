# Teste de automação (push → deploy)

**Estado: não executado.** A alteração está só no diretório local, sem commit nem push.

## Alteração

Arquivo `app/index.js`, badge da página inicial:

| Antes | Depois |
|---|---|
| `Deploy Status: Sucesso! ✅` | `Deploy realizado com sucesso pelo Azure DevOps!` |

## Roteiro

1. Abrir a aplicação pública e salvar o print com o badge antigo.
2. Fazer commit e push na `main`.
3. Conferir que uma nova Build foi iniciada sozinha, com o commit correspondente.
4. Conferir o novo Artifact `drop`.
5. Conferir que uma nova Release (Release-2) foi criada sozinha e que `Deploy-Producao` terminou com sucesso.
6. Recarregar a aplicação (Ctrl+F5) e salvar o print com o novo badge.
7. Guardar os prints em [09-automacao-git-push](../entregaveis/evidencias/09-automacao-git-push/).

## Registro (preencher após a execução)

| Item | Valor |
|---|---|
| Commit | Pendente |
| Build disparada automaticamente | Pendente |
| Release disparada automaticamente | Pendente |
| Página exibindo o novo badge | Pendente |

Se a Build ou a Release não disparar, verificar na interface o gatilho de CI da Build e o Continuous Deployment da Release. O workflow do GitHub Actions não participa deste teste.
