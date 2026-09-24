# Arautos Wiki

## O que é
Site estático wiki-style respondendo às acusações do documentário "Escravos da Fé" (HBO, 2026) contra os Arautos do Evangelho. Cada artigo responde a uma acusação específica com fatos documentados do livro "O Comissariado dos Arautos do Evangelho" e fontes externas verificáveis.

## Stack
- HTML estático + CSS + JavaScript vanilla
- Sem framework, sem build step
- Deploy: Cloudflare Pages (`arautos-wiki`) em arautos.integros.org, autodeploy via GitHub Actions

## Estrutura
- /*.html — Artigos da wiki (20 páginas interligadas)
- /css/wiki.css — Estilos compartilhados
- /js/ — Scripts (se necessário)

## Deploy
Cloudflare Pages, projeto `arautos-wiki` (arautos.integros.org).

**Autodeploy (desde 2026-09-24):** todo push em `main` roda `.github/workflows/deploy.yml` no GitHub Actions, que publica a pasta `.` via `wrangler pages deploy --branch=main`. Secrets `CLOUDFLARE_API_TOKEN` e `CLOUDFLARE_ACCOUNT_ID` ficam no repo.

- Publicar = commit + push em `main`. **Não** usar `wrangler pages deploy` manual: o que não estiver no Git é sobrescrito no próximo push.
- Republicar sem commit: `gh workflow run deploy.yml`. Acompanhar: `gh run list` / `gh run watch`.
- Não vão para o site: `CLAUDE.md`, `AGENTS.md`, `README.md`, `.github`, `.claude*`, `functions/`, `scripts/`, `test/`, `package*.json`, `wrangler.*`. Pages Functions em `functions/` continuam sendo compiladas normalmente.
- Guia geral: vault `30-tecnico/deploys-cloudflare.md`.

## Git
- Push direto na main (site estático, sem build costs)
- Conventional commits em inglês
