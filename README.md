# A Verdade Oculta — Site de RPG

Template de site estilo anos 90/2000 para campanha de RPG de mesa, hospedado via GitHub Pages + Jekyll.

## Como usar

### 1. Configurar o repositório

1. Faça um fork ou clone este repositório
2. Edite `_config.yml` com seu usuário e nome do repositório
3. Ative GitHub Pages nas configurações do repositório (Settings → Pages → Branch: main)

### 2. Escrever uma nova notícia/post

Crie um arquivo em `_posts/` com o formato de nome:

```
YYYY-MM-DD-titulo-do-post.md
```

Exemplo: `2025-03-10-novo-avistamento-zona-sul.md`

#### Cabeçalho do post (front matter)

```yaml
---
layout: post
title: "Título da Investigação"
date: 2025-03-10 23:30:00 -0300
tags: [governo, extraterrestre, financas, saude, militar]
classificado: true        # mostra o carimbo SECRETO (opcional)
fonte: "Descrição da fonte anônima"
excerpt: "Resumo curto que aparece na listagem principal."
---
```

#### Formatação do conteúdo (Markdown)

```markdown
## SUBTÍTULO DA SEÇÃO

Texto normal do parágrafo.

> Citação de fonte ou depoimento importante

**Palavra em destaque** e *texto em itálico (aparece em laranja)*

- Item de lista
- Outro item

---   ← linha divisória
```

### 3. Estrutura de arquivos

```
verdade-oculta/
├── _config.yml          ← configurações do site
├── index.html           ← página principal
├── _layouts/
│   ├── default.html     ← template base
│   └── post.html        ← template de post
├── _posts/
│   └── YYYY-MM-DD-*.md  ← suas notícias aqui
└── assets/
    └── css/
        └── style.css    ← visual do site
```

### 4. Personalizar o ticker de alertas

Edite a linha do ticker em `_layouts/default.html` para trocar as manchetes rolantes.

### 5. Testar localmente (opcional)

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
# Acesse http://localhost:4000
```

---

*Este site é ficção criada para uso em RPG de mesa.*
