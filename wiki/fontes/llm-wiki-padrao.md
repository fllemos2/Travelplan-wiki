---
tipo: fonte
titulo: LLM Wiki — Um Padrão para Bases de Conhecimento Pessoais
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, knowledge-management, llm, fundacao]
fontes: []
confianca: alta
status: ativo
autor: desconhecido
publicado: desconhecido
origem: colado pelo Fabio no chat
arquivo_raw: raw/2026-09-01-llm-wiki-padrao.md
---

# LLM Wiki — Um Padrão para Bases de Conhecimento Pessoais

> O documento fundador deste cofre. Descreve o padrão que este próprio cofre implementa: um LLM que constrói e mantém uma wiki persistente entre você e suas fontes brutas, em vez de re-derivar conhecimento a cada pergunta.

## Tese central

RAG re-descobre conhecimento do zero a cada query — nada se acumula. A alternativa é compilar o conhecimento **uma vez**, numa wiki de markdown interligada que o LLM mantém viva. As referências cruzadas já estão lá, as contradições já foram sinalizadas, a síntese já reflete tudo que foi lido. O artefato **compõe juros**: fica mais rico a cada fonte adicionada e a cada pergunta feita.

O motivo pelo qual isso funciona é econômico, não técnico: a parte tediosa de manter uma base de conhecimento nunca foi ler ou pensar — foi a **escrituração**. Humanos abandonam wikis porque o custo de manutenção cresce mais rápido que o valor. LLMs não se entediam, não esquecem de atualizar uma referência cruzada, e tocam 15 arquivos numa passada. A wiki sobrevive porque manter passou a custar quase nada.

## Pontos-chave

- **Três camadas:** fontes brutas (imutáveis, sua fonte da verdade) → wiki (100% escrita pelo LLM) → schema (`CLAUDE.md`, o arquivo de configuração que transforma o LLM num bibliotecário disciplinado em vez de um chatbot genérico). Ver [[arquitetura-tres-camadas]].
- **Três operações:** ingest, query, lint. Ver [[ciclo-ingest-query-lint]].
- **Divisão de trabalho:** o humano faz curadoria, direção e boas perguntas. O LLM faz todo o resto. Você quase nunca escreve na wiki.
- **Um ingest bom toca 10–15 páginas.** Ingerir não é indexar — é integrar: atualizar entidades, revisar sínteses, marcar onde o dado novo contradiz o antigo.
- **Respostas boas voltam para a wiki.** Uma comparação, uma análise, uma conexão descoberta — arquivar em vez de deixar morrer no histórico do chat. A exploração compõe igual à ingestão.
- **`index.md` + `log.md`** substituem infraestrutura de RAG por embeddings até ~100 fontes / centenas de páginas. Índice orientado a conteúdo, log orientado a tempo.
- **O documento é deliberadamente abstrato.** Estrutura de pastas, convenções e ferramentas devem ser instanciadas por cada um junto com seu agente. Tudo é opcional e modular.

## Ferramentas citadas

| Ferramenta | Para quê | Situação aqui |
|---|---|---|
| [[obsidian]] | Ler/navegar a wiki; graph view | Em uso — este cofre é um vault |
| Obsidian Web Clipper | Converter artigos web em markdown | Recomendado para alimentar `raw/` |
| Dataview (plugin) | Queries sobre o frontmatter | Viabilizado — nosso frontmatter é padronizado |
| Marp | Decks de slides a partir de markdown | Disponível como formato de resposta |
| qmd | Busca local BM25+vetorial sobre markdown | Só quando o `index.md` não der conta |
| git | Histórico de versão da wiki | **Ainda não configurado** |

## Conexões no cofre

- Estabelece [[wiki-compilada-vs-rag]] — a distinção que justifica todo o resto.
- Estabelece [[ciclo-ingest-query-lint]] — o loop operacional.
- Estabelece [[arquitetura-tres-camadas]] — a separação raw / wiki / schema.
- Situa [[memex]] como o ancestral intelectual da ideia.
- Define o papel de [[obsidian]] como interface de leitura.
- É a fonte de todo o `CLAUDE.md` deste cofre.

## Citações que valem guardar

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "Humans abandon wikis because the maintenance burden grows faster than the value."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## O que ficou em aberto

- **Escala.** O autor afirma que índice + log bastam até ~100 fontes, mas não mostra medição. Onde exatamente quebra? [inferência minha: o gargalo vem antes, quando o `index.md` deixa de caber confortavelmente numa leitura].
- **Qualidade da propagação.** "Um ingest toca 10–15 páginas" é métrica de esforço, não de acerto. O documento não oferece jeito de saber se a propagação foi *boa*.
- **Deriva de síntese.** Se o LLM revisa a tese a cada fonte, o que impede uma deriva lenta rumo ao que foi lido por último? Nosso `molde-sintese` tenta cobrir isso exigindo "o que derrubaria a tese".
- Autor e data de publicação desconhecidos — o texto chegou colado, sem procedência.
