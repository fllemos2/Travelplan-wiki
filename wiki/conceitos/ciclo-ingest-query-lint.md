---
tipo: conceito
titulo: Ciclo Ingest / Query / Lint
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, workflow, operacao]
fontes: ["[[llm-wiki-padrao]]"]
confianca: alta
status: ativo
---

# Ciclo Ingest / Query / Lint

> As três — e apenas três — operações que mantêm um LLM Wiki vivo. Tudo que fazemos neste cofre é uma delas.

## Como funciona

**Ingest** é escrita. Entra matéria-prima, sai wiki atualizada. O passo que define a operação não é escrever o resumo da fonte — é **propagar**: atualizar entidades, revisar sínteses, marcar contradições. Ingest que só cria uma página é indexação disfarçada, e recai em [[wiki-compilada-vs-rag]] do lado errado.

**Query** é leitura — mas com um retorno de escrita. Índice → páginas → resposta citada. E o detalhe que a maioria das pessoas perde: uma resposta boa é conhecimento novo, e deve voltar para o cofre como página. Sem isso, o trabalho de pensar escorre para o histórico do chat e evapora.

**Lint** é manutenção. É o que impede que a wiki apodreça enquanto cresce: órfãs, links quebrados, contradições esquecidas, afirmações que uma fonte nova já superou. Nenhuma dessas coisas aparece durante ingest ou query — só numa varredura dedicada.

```
        ┌──────────┐
  raw ──►  INGEST  ├──► wiki ◄──┐
        └──────────┘            │
                                │ arquiva resposta
        ┌──────────┐            │
 você ──►  QUERY   ├────────────┘
        └──────────┘
        ┌──────────┐
 tempo ─►   LINT   ├──► wiki (corrigida)
        └──────────┘
```

O ciclo tem duas realimentações: query alimenta a wiki (respostas arquivadas) e lint alimenta a curadoria (sugere fontes que faltam). É isso que faz o sistema compor em vez de só crescer.

## Evidência a favor

- [[llm-wiki-padrao]] descreve as três operações como suficientes; nada do que este cofre precisa fazer até agora caiu fora delas.

## Evidência contra / limites

- **Nenhuma métrica de qualidade.** O ciclo mede esforço ("tocou 12 páginas"), não acerto. Um ingest ruim e um bom deixam o mesmo rastro no log.
- **Lint depende de disciplina.** É a operação sem gatilho externo — ninguém *pede* um lint. Por isso o `CLAUDE.md` me obriga a propor um a cada ~10 ingests.

## Aplicação prática

É o esqueleto do `CLAUDE.md` (§3, §4, §5). Toda interação neste cofre se declara como uma dessas três — e o `log.md` registra qual foi.

## Conceitos vizinhos

- [[wiki-compilada-vs-rag]] — o *porquê* que o ciclo serve.
- [[arquitetura-tres-camadas]] — o *onde* que o ciclo opera.
