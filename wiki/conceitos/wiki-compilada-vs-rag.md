---
tipo: conceito
titulo: Wiki Compilada vs. RAG
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, llm, knowledge-management]
fontes: ["[[llm-wiki-padrao]]"]
confianca: alta
status: ativo
---

# Wiki Compilada vs. RAG

> Conhecimento pode ser **re-derivado a cada pergunta** (RAG) ou **compilado uma vez e mantido vivo** (wiki). A segunda opção acumula; a primeira não.

## Como funciona

RAG é *lazy evaluation*: os documentos ficam crus, e a síntese acontece no momento da query, sob pressão de tempo e de janela de contexto. Toda pergunta paga o custo inteiro de encontrar e costurar os fragmentos, e o resultado é jogado fora depois.

A wiki compilada é *eager evaluation com cache persistente*: o custo de síntese é pago no momento da **ingestão**, quando há tempo e atenção, e o resultado vira artefato em disco. A query depois só lê.

A consequência importante não é velocidade — é **acumulação**. Como o artefato persiste, a fonte nº 40 pode ser confrontada com o que as 39 anteriores deixaram escrito. No RAG isso não acontece: a fonte nº 40 é só mais um chunk num índice plano, e ninguém nunca percebe que ela contradiz a nº 12.

| | RAG | Wiki compilada |
|---|---|---|
| Quando sintetiza | Na query | Na ingestão |
| Onde mora o resultado | Efêmero | Em disco, versionado |
| Contradição entre fontes | Invisível | Detectada e marcada na ingestão |
| Custo da 100ª pergunta | Igual ao da 1ª | Menor — está escrito |
| Inspecionável por humano | Não | Sim, é markdown |
| Custo de manutenção | Zero | Alto para humano, ~zero para LLM |

## Evidência a favor

- O argumento econômico de [[llm-wiki-padrao]]: o custo de manutenção — não o de leitura — é o que mata wikis humanas, e é exatamente o custo que o LLM zera.
- O artefato ser markdown puro significa que ele é auditável, versionável em git, e legível sem o LLM presente. O conhecimento não fica refém da ferramenta.

## Evidência contra / limites

- **Custo de compilação antecipada.** Se 90% das fontes nunca forem consultadas, RAG é mais barato. A wiki só compensa onde há retorno repetido ao material.
- **Compilação é lossy.** O que eu decidi não escrever na página, some da prática. `raw/` continua lá como rede de segurança, mas na prática ninguém volta nele.
- **Deriva.** Reescrever a mesma página muitas vezes pode afastá-la gradualmente das fontes. Mitigação: frontmatter `fontes:` obrigatório e o lint periódico.
- **Não é ou/ou.** Buscar em `raw/` durante uma query é sempre permitido — a wiki é a primeira parada, não a única.

## Aplicação prática

Explica por que o passo 4 do ingest (propagar pelo cofre) é o passo que não pode ser pulado. Sem propagação, isto vira RAG com passos extras.

## Conceitos vizinhos

- [[ciclo-ingest-query-lint]] — o mecanismo operacional que mantém a compilação em dia.
- [[arquitetura-tres-camadas]] — a separação que impede a compilação de destruir o original.
- [[memex]] — a mesma intuição, 80 anos antes, sem quem fizesse a manutenção.
