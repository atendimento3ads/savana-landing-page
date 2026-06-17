# Savana — Landing Pages (JUN26)

Landing pages de conversão da **Savana Distribuidora de Auto Peças**, em HTML/CSS estático (sem build, sem dependências).

## Estrutura

```
site/
├── index.html              # Hub — links para as 3 LPs
├── assets/                 # Logo do hub
├── caminhao/               # LP Caminhão (linha pesada diesel)
│   ├── index.html
│   └── assets/
├── caminhonetes/           # LP Caminhonetes (linha leve / picape)
│   ├── index.html
│   └── assets/
└── maquinas-agricolas/     # LP Máquinas Agrícolas (linha agrícola)
    ├── index.html
    └── assets/
```

Cada LP é independente e autossuficiente (HTML único + pasta `assets/` com imagens). Os caminhos são relativos, então funcionam em qualquer subdiretório.

## URLs (após deploy no GitHub Pages)

- `/` — hub
- `/caminhao/`
- `/caminhonetes/`
- `/maquinas-agricolas/`

## Deploy (GitHub Pages)

1. Crie um repositório no GitHub com a conta desejada.
2. Suba o conteúdo desta pasta (`site/`) para a raiz do repositório.
3. Em **Settings → Pages**, selecione a branch (ex.: `main`) e a pasta `/ (root)`.
4. As páginas ficarão disponíveis nas URLs acima.

> Observação: para GitHub Pages gratuito, o repositório precisa ser **público** (repositórios privados exigem plano pago).

---
Desenvolvido por 3ADS.
