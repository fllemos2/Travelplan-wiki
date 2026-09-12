---
tipo: conceito
titulo: Arquitetura de Três Camadas
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, arquitetura]
fontes: ["[[llm-wiki-padrao]]"]
confianca: alta
status: ativo
---

# Arquitetura de Três Camadas

> Fontes brutas, wiki e schema são camadas com **donos diferentes**. A separação é o que permite compilar agressivamente sem risco de perder o original.

## Como funciona

| Camada | Dono | Mutabilidade | Papel |
|---|---|---|---|
| `raw/` | O Fabio | Imutável para mim | Fonte da verdade. Rede de segurança da compilação. |
| `wiki/` | Eu | Reescrita livre | O artefato compilado. Descartável em princípio — reconstruível a partir de `raw/`. |
| `CLAUDE.md` | Nós dois | Evolui devagar | Define *como* compilar. Sem ele, um chatbot genérico. |

A relação entre as camadas é a de um compilador: `raw/` é o código-fonte, `wiki/` é o binário, `CLAUDE.md` é o compilador. Isso dá uma propriedade valiosa — **posso reescrever `wiki/` sem medo**, porque a verdade nunca esteve lá. Se uma reorganização der errado, o material original está intacto.

A camada de schema é a menos óbvia e a mais decisiva. É o que faz a diferença entre "LLM que responde sobre arquivos" e "bibliotecário disciplinado com convenções estáveis". Ela evolui: sempre que descobrimos uma regra que funciona, ela sobe para o `CLAUDE.md` e vale para todas as sessões futuras.

## Evidência a favor

- [[llm-wiki-padrao]] nomeia o schema como "the key configuration file" e atribui a ele a diferença entre bibliotecário e chatbot.
- A imutabilidade de `raw/` é o que torna a auditoria possível: toda afirmação da wiki deve ser rastreável até um arquivo que ninguém reescreveu.

## Evidência contra / limites

- **"Reconstruível a partir de raw/" é só parcialmente verdade.** A wiki também contém as *minhas* sínteses e as *suas* perguntas — isso não está em `raw/` e se perderia numa reconstrução. Daí `wiki/sintese/` e `wiki/consultas/` merecerem cuidado extra (e git).
- Se o Fabio começar a escrever direto na wiki, a fronteira de propriedade borra e eu passo a poder sobrescrever o trabalho dele. Combinado: ele comenta, eu escrevo.

## Aplicação prática

É o motivo da regra dura no `CLAUDE.md` §8: *`raw/` é sagrado, não toco*. E do porquê o schema é um arquivo do cofre, não uma instrução de chat — instrução de chat morre com a sessão.

## Conceitos vizinhos

- [[wiki-compilada-vs-rag]] — o que a camada do meio existe para fazer.
- [[ciclo-ingest-query-lint]] — as operações que atravessam as camadas.
