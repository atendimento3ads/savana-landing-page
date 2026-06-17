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

## URLs (produção)

- `https://savanadist.com.br/` — hub
- `https://savanadist.com.br/caminhao/`
- `https://savanadist.com.br/caminhonetes/`
- `https://savanadist.com.br/maquinas-agricolas/`

## Recursos

- **WhatsApp:** todos os botões abrem o WhatsApp `(92) 99183-3602` com uma mensagem
  personalizada por contexto (peça específica, modelo, orçamento geral ou urgência).
- **FAQ em sanfona:** abrir uma pergunta fecha as demais.
- **Parallax adaptativo:** efeito sutil no hero, desativado automaticamente em conexão
  lenta, modo economia de dados, pouca memória, toque/mobile ou `prefers-reduced-motion`.
- **Responsivo:** widescreen, desktop, notebook, tablet e celular.
- **SEO/GEO:** meta tags, Open Graph, canonical, geo tags e dados estruturados JSON-LD
  (`AutoPartsStore`, `BreadcrumbList`, `FAQPage`).
- **Performance:** CSS inline, fonte não-bloqueante, `preload`/`fetchpriority` do hero,
  `width`/`height` nas imagens (anti-CLS), `loading="lazy"` abaixo da dobra e `.htaccess`
  com compressão (gzip/brotli) e cache de longo prazo para estáticos.

## Deploy (GitHub → Git Version Control da HostGator)

O arquivo [`.cpanel.yml`](.cpanel.yml) define a publicação automática para o document root
do domínio (`/home2/hg3ads37/savanadist.com.br/`).

1. **cPanel → Git™ Version Control → Create** com *Clone a Repository* ligado.
   - Clone URL: `https://github.com/atendimento3ads/savana-landing-page.git`
   - Repository Path: `/home2/hg3ads37/repositories/savana-landing-page`
2. Em **Manage → Pull or Deploy**: **Update from Remote** e depois **Deploy HEAD Commit**.

Para publicar mudanças: `git push` aqui e repita o passo 2 no cPanel.

---
Desenvolvido por 3ADS.
