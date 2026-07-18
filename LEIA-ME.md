# Workshop de Sono — Landing Page
## Corpore × MEV Vale | 26/07/2026

---

## Como rodar localmente

```bash
# 1. Instale as dependências
npm install

# 2. Suba o servidor de desenvolvimento
npm run dev
# → Abra http://localhost:4321
```

---

## Como gerar o site para Hostinger

```bash
# Gera a pasta dist/ com o site estático
npm run build

# (Opcional) Pré-visualize o build antes de subir
npm run preview
```

Depois do build, **faça upload da pasta `dist/`** para o painel da Hostinger (File Manager ou FTP).

---

## Antes de fazer o build — Logos

Copie os logos para a pasta `public/`:

| Arquivo | Origem |
|---|---|
| `logo-branco.png` | `C:\Users\User\Desktop\Claude-Code\corpore-health-map\assets\images\logos\logo-branco.png` |
| `logo-amarelo-icone.png` | `C:\Users\User\Desktop\Claude-Code\corpore-health-map\assets\images\logos\logo-amarelo-icone.png` |

> O site funciona sem os logos (há fallbacks em texto), mas ficará melhor com eles.

---

## Estrutura de arquivos

```
landing-page/
├── public/
│   ├── logo-branco.png          ← copiar manualmente
│   └── logo-amarelo-icone.png   ← copiar manualmente
├── src/
│   ├── layouts/
│   │   └── Layout.astro         ← HTML base, meta tags, schema
│   ├── pages/
│   │   └── index.astro          ← página principal (todos os 7 blocos)
│   └── styles/
│       └── global.css           ← design system, cores, animações
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

---

## Cores usadas

| Variável | Hex | Uso |
|---|---|---|
| `--color-charcoal` | `#3e3e3d` | Fundo escuro, texto principal |
| `--color-blue` | `#46799a` | Corpore azul, detalhes |
| `--color-yellow` | `#e2de1e` | CTA, destaques, logo |
| `--color-teal` | `#00B4C8` | MEV Vale, labels, badges |
| `--color-offwhite` | `#F5F5F3` | Fundo seções claras |

---

## Link de inscrição

Está definido no topo do `src/pages/index.astro`:

```js
const LINK_INSCRICAO = "https://corporetraininggym.com.br/link/workshop-sono/";
```

Para alterar, basta editar essa linha.

---

*Corpore Training Gym × MEV Vale — Workshop de Sono · 26/07/2026*
