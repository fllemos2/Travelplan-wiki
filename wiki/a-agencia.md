---
tipo: overview
titulo: A Agência — estrutura de trabalho
criado: 2026-09-01
atualizado: 2026-09-01
tags: [meta, agencia, equipe, workflow]
fontes: ["[[briefing-fundador]]"]
confianca: alta
status: ativo
---

# A Agência — estrutura de trabalho

> Seis funcionários. Não são personagens: cada um é um subagente real definido em `.claude/agents/`, com ferramentas próprias, regras próprias e uma pasta do cofre sob sua responsabilidade.

## Quadro de funcionários

| Funcionário | O que faz | Pasta | O erro que ele existe para evitar |
|---|---|---|---|
| **Controlador Financeiro** | custo-alvo, curva de poupança, veredito de orçamento | `wiki/financeiro/` | a família sonhar sem aritmética |
| **Caçador de Ofertas** | preços, monitoramento, histórico, dossiê de execução | `wiki/ofertas/` | comprar preço normal achando que é promoção |
| **Curador de Destinos** | destinos, melhor época, adequação ao perfil | `wiki/destinos/` | ir no lugar certo no mês errado |
| **Arquiteto de Roteiro** | dia a dia, passeios, translados, 3 variações | `wiki/roteiros/` | roteiro cheio demais, família exausta |
| **Despachante** | passaporte, visto, vacina, seguro, prazos | `wiki/logistica/` | descobrir o passaporte vencido faltando um mês |
| **Concierge Visual** | apresentação, fotos reais, material para decidir | Artifacts + `raw/assets/` | o sonho esfriar durante os meses de poupança |

Eu (o gerente) coordeno, converso com você, e mantenho o cofre. Você não precisa saber quem chamar — descreva o que quer e eu aciono. Mas se quiser chamar direto: *"chama o caçador de ofertas para..."*.

## A ordem de trabalho importa

O erro clássico de planejamento de viagem é começar pelo roteiro. Aqui a sequência é deliberada:

```
1. O SONHO        → o que a família quer sentir            (você)
2. FINANCEIRO     → custo-alvo e a data em que é possível  (Controlador)   ← a restrição real
3. DESTINO        → onde e em que mês, dado o teto          (Curador)
4. VIGILÂNCIA     → gatilhos armados, monitoramento         (Caçador)      ← roda em paralelo, por meses
5. PRAZOS         → linha do tempo regressiva               (Despachante)  ← começa cedo, não no fim
6. ROTEIRO        → dia a dia em 3 variações                (Arquiteto)
7. APRESENTAÇÃO   → o sonho visível                         (Concierge)
```

Os passos 1–3 travam tudo. O passo 4 roda em segundo plano do começo ao fim. O passo 7 não é o último em importância — é o que sustenta a moral da família durante os meses do passo 4.

## Ritmo de operação

| Quando | O quê |
|---|---|
| **Agora** | preencher o briefing em [[o-sonho]] |
| **Semanal** | caçador varre preços → `historico-de-precos`; olhar o `checklist-prazos` |
| **Mensal** | controlador atualiza a curva de poupança; concierge atualiza a apresentação |
| **Quando um gatilho bate** | alerta + dossiê de execução em minutos ([[regras-de-compra]]) |
| **A cada ~10 ingests** | lint do cofre |

## Vigilância automática

O monitoramento de preços pode rodar de verdade, sem eu ser acionado toda vez: `/schedule` cria um agente em nuvem num cron, `/loop` roda em intervalo dentro de uma sessão. Configuramos quando os gatilhos estiverem armados — vigiar antes de ter teto de preço é só gastar ciclo.

## O limite honesto da agência

**A agência não compra.** Eu decido, você clica. Isso está detalhado em [[regras-de-compra]] e não é negociável por bom senso: um erro meu numa busca custa cinco minutos, um erro meu num checkout custa a passagem da família inteira.

## Relacionadas

- [[o-sonho]] — a missão · [[plano-de-viabilidade]] — a aritmética · [[overview]] — o cofre
