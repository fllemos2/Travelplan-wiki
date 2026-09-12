---
tipo: overview
titulo: Visão Geral do Cofre
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, entrada]
fontes: ["[[llm-wiki-padrao]]", "[[briefing-fundador]]"]
confianca: alta
status: ativo
---

# Visão Geral do Cofre

> A porta de entrada. Se você abriu este cofre sem contexto, comece aqui.

## O que é isto

O **centro de operações de uma viagem** — a viagem que a família Lemos hoje considera um sonho distante por limitação financeira.

Não é um caderno de anotações de viagem. É um projeto com orçamento, prazos e uma tese a ser provada: **a viagem não é impossível, ela está mal datada**. Ver [[o-sonho]].

Tecnicamente, é um LLM Wiki: o Fabio traz fontes e decisões, eu compilo tudo em páginas markdown interligadas e mantenho consistente ao longo dos meses. As regras estão em [[CLAUDE|CLAUDE.md]] — §1 a §8 é o método, §9 é este domínio.

## Por onde começar

1. [[o-sonho]] — a missão e os campos que ainda faltam. **É aqui que o projeto está travado.**
2. [[a-agencia]] — os seis funcionários e a ordem de trabalho.
3. [[regras-de-compra]] — o que a agência executa e o que não executa.

## Mapa

**Operação da viagem**
- [[o-sonho]] — a tese e o briefing · [[plano-de-viabilidade]] — a aritmética
- [[historico-de-precos]] — linha de base e gatilhos · [[checklist-prazos]] — prazos regressivos
- [[regras-de-compra]] — o limite honesto da agência
- `wiki/destinos/`, `wiki/roteiros/` — vazios, esperando destino e teto

**Método** (do [[llm-wiki-padrao]])
- [[wiki-compilada-vs-rag]] · [[ciclo-ingest-query-lint]] · [[arquitetura-tres-camadas]]
- [[obsidian]] — a interface de leitura · [[memex]] — o ancestral de 1945

## Como usar

| Você quer | Diga |
|---|---|
| Adicionar informação (comprovante, print, artigo, ideia) | jogue em `raw/` ou cole, e peça o ingest |
| Perguntar qualquer coisa | só pergunte — eu leio o índice antes de responder |
| Acionar um funcionário específico | *"chama o caçador de ofertas para..."* |
| Verificar a saúde do cofre | "lint" |
| Mudar as regras | *"muda o schema: ..."* |

## Estado do projeto

- [x] Cofre e método instalados
- [x] Domínio definido; 6 funcionários contratados
- [x] Estrutura financeira, de ofertas e de prazos criada (esqueletos)
- [ ] **Briefing preenchido** — 10 campos em [[o-sonho]] · **trava tudo**
- [ ] Custo-alvo e data de viabilidade
- [ ] Gatilhos de preço armados e vigilância ligada
- [ ] Git inicializado
- [ ] Obsidian: Templates → `meta/templates/`; anexos → `raw/assets/`
