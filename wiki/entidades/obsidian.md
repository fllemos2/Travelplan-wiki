---
tipo: entidade
titulo: Obsidian
criado: 2026-09-01
atualizado: 2026-09-01
tags: [ferramenta, meta]
fontes: ["[[llm-wiki-padrao]]"]
confianca: alta
status: ativo
categoria: ferramenta
---

# Obsidian

> Editor de markdown local com links bidirecionais. Aqui, ele é a **interface de leitura** do cofre — eu escrevo, o Fabio navega.

## O que se sabe

- Trabalha sobre uma pasta de arquivos `.md` no disco ("vault"). Sem banco de dados, sem lock-in — [[llm-wiki-padrao]].
- Links `[[wiki-style]]` geram backlinks automáticos e alimentam o **graph view**, que é o melhor jeito de ver a forma do cofre: quem é hub, quem é órfã, o que está desconectado.
- Plugins relevantes citados na fonte: **Web Clipper** (artigo web → markdown, para alimentar `raw/`), **Dataview** (queries sobre frontmatter → tabelas dinâmicas), **Marp** (slides a partir de markdown).
- O Web Clipper baixa imagens localmente se "Attachment folder path" apontar para uma pasta fixa (recomendado: `raw/assets/`) e "Download attachments for current file" estiver mapeado num atalho.

## Papel no meu contexto

A analogia da fonte é a que vale: **Obsidian é a IDE, eu sou o programador, a wiki é o codebase**. O fluxo pretendido é o agente de um lado da tela e o Obsidian do outro — eu edito, o Fabio vê os links e o grafo mudarem em tempo real.

Nosso frontmatter padronizado ([[CLAUDE|schema]] §2) foi desenhado pensando no Dataview: `tipo`, `tags`, `confianca` e `status` são todos consultáveis.

## Estado neste cofre

| Item | Situação |
|---|---|
| Vault | `C:\Apps\52-TravelPlan\Travel-Plan` — ativo |
| Plugins core | file-explorer, graph, backlink, properties, templates, canvas, sync — ligados |
| Templates | Pasta `meta/templates/` criada; **falta apontar o plugin Templates para ela** |
| Web Clipper | Não configurado |
| Dataview | Não instalado (é plugin da comunidade) |
| Attachment path | Não configurado — deveria ser `raw/assets/` |

## Lacunas

- O Obsidian Sync está ligado no vault; não sei se está de fato sincronizando nem para onde.
- Nunca verifiquei como o Obsidian se comporta com o `.obsidian/` sob git, se formos versionar.
