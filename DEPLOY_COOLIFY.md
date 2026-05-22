# Deploy no Coolify com Nixpacks

Este repositório já está preparado para deploy estático no Coolify usando `Nixpacks`.

## Arquivos de deploy

- `nixpacks.toml`
  Gera uma pasta `dist/` durante o build, copiando:
  - `index.html`
  - `styles/`
  - arquivos estáticos na raiz, como PDFs e imagens
- `.gitignore`
  Ignora `dist/`, que é apenas artefato de build

## Configuração recomendada no Coolify

1. `Build Pack`: `Nixpacks`
2. `Base Directory`: `/`
3. Ativar `Is it a static site?`
4. `Publish Directory`: `/dist`

## Observações

- Como o site é HTML/CSS puro, não existe etapa de instalação de dependências.
- O PDF referenciado na página também entra em `dist/`, então o link continua funcionando no deploy.
- Se você criar novas pastas de assets fora de `styles/`, prefira usar nomes como `assets/`, `img/`, `images/` ou `public/`, porque elas já estão cobertas pelo build.
