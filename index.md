# Índice

Catálogo de tudo que existe no cofre. Atualizado a cada ingest. Primeira parada de toda query.

**Estado:** 5 fontes · 21 páginas · 6 funcionários · atualizado em 2026-09-13
**Domínio:** Agência de Viagem Particular — viabilizar a viagem de família dos Lemos
**🎯 A viagem:** Itália · Suíça · Disneyland Paris — **set/2028** (janela 10/set–15/out) — ~R$ 55.800

---

## Entrada

- [[wiki/overview|Visão Geral do Cofre]] — porta de entrada: o que é este cofre e onde está cada coisa.
- [[wiki/a-agencia|A Agência]] — os 6 funcionários, o que cada um evita, e a ordem de trabalho que não se inverte.

## A missão

- [[wiki/sintese/o-sonho|O Sonho]] — **a página central.** Quem viaja, para onde, quando e por quanto. A tese v1: a viagem é setembro de 2028. `confianca: media`
- [[wiki/roteiros/rota-mestra|A Rota Mestra]] — a descoberta que define a viagem: os três sonhos formam uma linha reta, Milão → Suíça → Paris. `alta`
- [[wiki/consultas/melhor-epoca|A Melhor Época]] — por que fim de setembro, critério por critério. Inclui o que a flexibilidade do homeschooling compra em dinheiro. `media`

## Financeiro

- [[wiki/financeiro/estrategia-livelo|Estratégia Livelo]] — saldo real confirmado: **79.479 pontos, sem expiração** ([[wiki/fontes/extrato-livelo|extrato 13/09]]). Cobre um trecho (~R$ 2.200–4.000) sem aporte; com aporte, ~R$ 5.500. `media`
- [[wiki/financeiro/plano-de-viabilidade|Plano de Viabilidade]] — **a data: setembro de 2028.** Custo-alvo em 3 cenários (~R$ 43k / 55,8k / 74k), as 6 alavancas que fecham a diferença, e a linha do tempo do dinheiro. `media`

## Ofertas

- [[wiki/ofertas/historico-de-precos|Histórico de Preços]] — primeiras âncoras da rota GIG–Milão. Gatilho nº 1 criado, janela ampliada, **pausado até out/2027** (cias vendem ~330 dias à frente).

## Logística

- [[wiki/logistica/regras-de-compra|Regras de Compra]] — **leia esta.** O que eu posso e não posso executar; por que eu não compro; e o dossiê de execução que resolve o problema de outro jeito.
- [[wiki/logistica/checklist-prazos|Checklist de Prazos]] — linha do tempo regressiva a partir de set/2028. Passaportes ✅; extrato Livelo ✅ (13/09); **ETIAS** é o item a vigiar.

## Destinos

*(vazio — próximo trabalho do `curador-destinos`: onde exatamente no norte da Itália e na Suíça)*

## Roteiros

- [[wiki/roteiros/rota-mestra|A Rota Mestra]] — o corredor Milão → Suíça → Paris e por que a ordem é essa.
- *Dia a dia e as 3 variações: pendentes, dependem da definição das cidades.*

## Conceitos — metodologia

- [[wiki/conceitos/wiki-compilada-vs-rag|Wiki Compilada vs. RAG]] — compilar o conhecimento uma vez em vez de re-derivá-lo a cada pergunta. `alta`
- [[wiki/conceitos/ciclo-ingest-query-lint|Ciclo Ingest / Query / Lint]] — as três operações que mantêm o cofre vivo. `alta`
- [[wiki/conceitos/arquitetura-tres-camadas|Arquitetura de Três Camadas]] — raw / wiki / schema como compilador. `alta`

## Entidades

- [[wiki/entidades/obsidian|Obsidian]] — a interface de leitura do cofre; inclui o que falta configurar. `ferramenta`
- [[wiki/entidades/memex|Memex (1945)]] — o ancestral da ideia. `historico` · `media`

## Fontes

- [[wiki/fontes/briefing-fundador|Briefing Fundador]] — o Fabio define a missão da agência; o que foi pedido e a única coisa que eu recusei. `2026-09-01`
- **Briefing completo** — `raw/2026-09-01-briefing-completo.md`: família, origem, poupança, destinos, janela e padrão de viagem. *(fonte lida direto; conteúdo compilado em [[wiki/sintese/o-sonho|O Sonho]])* `2026-09-01`
- [[wiki/fontes/llm-wiki-padrao|LLM Wiki — Um Padrão para Bases de Conhecimento Pessoais]] — documento fundador do método. `2026-09-01`
- [[wiki/fontes/extrato-livelo|Extrato Livelo — 13/09/2026]] — saldo real 79.479 pts, sem expiração; resolve a tarefa urgente do checklist. `2026-09-13`

## Consultas arquivadas

- [[wiki/consultas/melhor-epoca|A Melhor Época]] — resposta à pergunta "qual a melhor janela do ano". `2026-09-01`
- [[wiki/consultas/relatorio-mensal-2026-09|Relatório Mensal — Setembro/2026]] — primeiro relatório visual do concierge, com fotos reais de Lauterbrunnen, Zermatt e Langhe. `2026-09-13`

---

## Funcionários — `.claude/agents/`

| Nome para invocar | Papel |
|---|---|
| `controlador-financeiro` | custo-alvo, curva de poupança, veredito de orçamento |
| `cacador-ofertas` | preços, monitoramento, dossiê de execução |
| `curador-destinos` | destinos, melhor época, adequação ao perfil |
| `arquiteto-roteiro` | dia a dia, passeios, translados, 3 variações |
| `despachante` | passaporte, visto, vacina, seguro, prazos |
| `concierge-visual` | apresentação com fotos reais, material de decisão |

## Controle

- [[CLAUDE|CLAUDE.md]] — o schema, agora com §9 (o domínio).
- [[log|log.md]] — histórico cronológico.
- [[hot-cache|hot-cache.md]] — memória quente entre sessões.
- `meta/templates/` — [[meta/templates/molde-fonte|fonte]] · [[meta/templates/molde-entidade|entidade]] · [[meta/templates/molde-conceito|conceito]] · [[meta/templates/molde-sintese|síntese]]
- `meta/lint/` — relatórios de saúde *(vazio)*
