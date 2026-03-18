# Arautos Wiki

## O que é
Site estático wiki-style respondendo às acusações do documentário "Escravos da Fé" (HBO, 2026) contra os Arautos do Evangelho. Cada artigo responde a uma acusação específica com fatos documentados do livro "O Comissariado dos Arautos do Evangelho" e fontes externas verificáveis.

## Stack
- HTML estático + CSS + JavaScript vanilla
- Sem framework, sem build step
- Deploy: DigitalOcean (Nginx) em arautos.integros.org

## Estrutura
- /*.html — Artigos da wiki (20 páginas interligadas)
- /css/wiki.css — Estilos compartilhados
- /js/ — Scripts (se necessário)

## Deploy
- Servidor: 138.197.123.132 (porta SSH 2299, user deploy)
- Domínio: arautos.integros.org
- Servido por Nginx como site estático

## Git
- Push direto na main (site estático, sem build costs)
- Conventional commits em inglês
