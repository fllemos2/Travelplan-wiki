---
tipo: conceito
titulo: Histórico de Preços
criado: 2026-09-01
atualizado: 2026-09-18
tags: [ofertas, precos, vigilancia]
fontes: []
confianca: alta
status: ativo
---

# Histórico de Preços

> Preço sem histórico não é informação. Este arquivo é o que, daqui a três meses, permite reconhecer uma oferta de verdade em dez segundos — e ignorar a contagem regressiva na tela.

Alimentado pelo [[cacador-ofertas]] em **toda** consulta, inclusive quando o preço está ruim. Principalmente quando está ruim: é o preço ruim que estabelece a linha de base.

## Passagens

| Data/hora | Rota | Ida–Volta | Pax | Cia | Preço/pessoa | Total c/ taxas | Bagagem | Fonte |
|---|---|---|---|---|---|---|---|---|
| 2026-09-01 | GIG–MIL | i/v, baixa temporada | 1 | LATAM | a partir de R$ 4.457 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Milao-MIL) |
| 2026-09-01 | GIG–MIL | i/v, baixa temporada | 1 | ITA Airways | a partir de R$ 4.577 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Milao-MIL) |
| 2026-09-01 | GIG–MIL | i/v, baixa temporada | 1 | Lufthansa | a partir de R$ 4.750 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Milao-MIL) |
| 2026-09-18 | GIG–MIL | i/v, sem data específica | 1 | KAYAK (teaser de rota) | a partir de R$ 2.062 (provável tarifa de ida isolada, não i/v) | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Milao-MIL) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–FCO (Roma) | i/v, sem data específica | 1 | TAP Air Portugal | a partir de R$ 4.574 | não apurado | não apurado | [Google Flights](https://www.google.com/travel/flights/flights-from-rio-de-janeiro-to-rome.html?gl=BR&hl=pt-BR) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–FCO (Roma) | i/v, sem data específica | 1 | ITA Airways | a partir de R$ 4.727 | não apurado | não apurado | [ITA Airways](https://www.ita-airways.com/lhg/br/pt/o-d/cy-cy/rio-de-janeiro-roma) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–FCO (Roma) | i/v, sem data específica | 1 | não identificada | a partir de R$ 4.731 | não apurado | não apurado | [Decolar](https://www.decolar.com/passagens-aereas/rio/rom/passagens-aereas-para-roma-saindo-de-rio+de+janeiro) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–VCE (Veneza) | i/v, "últimos 5 dias" (indefinido) | 1 | ITA Airways | a partir de R$ 4.800 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Veneza-Marco-Polo-VCE) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–VCE (Veneza) | i/v, "últimos 5 dias" (indefinido) | 1 | TAP Air Portugal | a partir de R$ 4.825 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Rio-de-Janeiro-Galeao-Internacional-GIG/Veneza-Marco-Polo-VCE) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–VCE (Veneza) | i/v, sem data específica | 1 | SWISS | a partir de R$ 4.606 | não apurado | não apurado | [SWISS](https://www.swiss.com/lhg/br/pt/o-d/cy-cy/rio-de-janeiro-veneza) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | CDG–GIG (Paris→Rio, perna de volta) | i/v ou apenas ida, ambíguo | 1 | KAYAK (teaser de rota) | a partir de R$ 3.147 | não apurado | não apurado | [KAYAK](https://www.kayak.com.br/voos/Paris-Charles-de-Gaulle-CDG/Rio-de-Janeiro-Galeao-Internacional-GIG) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–PAR (Paris, referência p/ CDG) | i/v, sem data específica | 1 | Air France/KLM | a partir de R$ 5.243 | não apurado | não apurado | [Google Flights](https://www.google.com/travel/flights/flights-from-paris-to-rio-de-janeiro.html?gl=BR&hl=pt-BR) — via WebSearch, WebFetch bloqueado |
| 2026-09-18 | GIG–PAR (Paris, referência p/ CDG) | i/v, sem data específica | 1 | Avianca | a partir de R$ 4.617 | não apurado | não apurado | Google Flights (mesma busca acima) — via WebSearch, WebFetch bloqueado |

> ⚠️ As linhas acima são **âncoras de dimensionamento**, não ofertas: são preços "a partir de", sem taxas, sem bagagem e sem data específica. Servem só para calibrar o orçamento em [[plano-de-viabilidade]]. Ninguém compra com base nelas.

### 🚫 Tentativa de coleta 2026-09-18 — falha sistêmica de acesso direto

Nesta sessão o `cacador-ofertas` tentou obter cotações **reais, com data específica (ago–set/2027) e para 3 passageiros com bagagem despachada**, na ordem de prioridade pedida (Hopper/Kiwi.com → KAYAK → Skyscanner → Google Flights), para as rotas:

- GIG→MXP (Milão) · CDG→GIG (Paris, perna de volta do open-jaw)
- GIG→FCO (Roma) · GIG→VCE (Veneza) — alternativas de entrada

**Resultado: todas as tentativas de `WebFetch` falharam com `EGRESS_BLOCKED`** (proxy de rede do ambiente bloqueia o domínio), nos seguintes domínios: `kayak.com.br`, `google.com` (Google Flights), `skyscanner.com.br`, `kiwi.com`, `mundi.com.br`, `esky.eu`, `latamairlines.com`, e até um domínio de controle neutro (`en.wikipedia.org`) — o que confirma que é um **bloqueio sistêmico da infraestrutura desta execução**, não um bloqueio específico de site de viagem. Sem acesso direto à página, não há como inserir datas específicas (ago–set/2027), número de passageiros (3) ou bagagem despachada em nenhuma busca — essas ferramentas exigem interação com formulário/JS que o `WebFetch` não consegue simular sem primeiro carregar a página.

**O que sobrou:** `WebSearch` (que não foi bloqueado) devolveu apenas **snippets agregados e cacheados** dessas mesmas páginas — preços "a partir de", sem data confirmada, sem confirmação de ida-e-volta vs. só-ida em vários casos, e para 1 passageiro (não 3). Esses números foram logados na tabela acima **apenas como âncoras adicionais de rota**, no mesmo espírito de baixa confiança das 3 âncoras originais de 01/09 — **não são dado de linha de base para ago–set/2027** e não autorizam nenhum veredito de compra.

- Todas as buscas por `"agosto 2027"` / `"setembro 2027"` retornaram explicitamente **sem dado específico** para essas datas — os próprios mecanismos de busca confirmaram que não há cobertura de preço tão distante no tempo.
- **Nenhuma busca retornou dado de setembro/2028** (nem foi tentada — não faria sentido, já que a venda só abre em ~out/2027). Não houve, portanto, nenhum alerta crítico de abertura antecipada.
- **Veredito da sessão: PASSA.** Não há dado sólido o suficiente para comparar com o teto de R$ 4.457/pessoa, nem para armar ou reavaliar o gatilho de [[historico-de-precos|compra]]. A pendência central — linha de base real de ago–set/2027 — continua em aberto.

**Pendência para a próxima execução agendada:** se o bloqueio de `WebFetch` persistir, a coleta autônoma via este agente fica estruturalmente limitada a snippets de `WebSearch` (baixa confiança). Vale avaliar com o Fabio: (a) configurar alerta de tarifa nativo do Google Flights/KAYAK (ver [[regras-de-compra]], seção "Exceção que vale discutir depois"), que não depende de `WebFetch`; ou (b) tentar de novo em ciclos futuros, caso o proxy mude de configuração.

## Hospedagem

| Data/hora | Cidade | Local | Diária | Noites | Total | Cancelamento | Cozinha | Fonte |
|---|---|---|---|---|---|---|---|---|
| — | | | | | | | | |

## Linha de base por rota

Preencher quando houver ~5 observações. É o resumo que se consulta na hora da decisão.

| Rota | Mín. visto | Mediana | Máx. visto | Melhor mês | "É oferta abaixo de" |
|---|---|---|---|---|---|
| **GIG→MXP / CDG→GIG** *(open-jaw, a rota da viagem)* | — | — | — | set/out (a confirmar) | — |
| GIG–MIL (i/v simples, referência) | R$ 4.457 | R$ 4.577 *(3 obs. de baixa confiança)* | R$ 4.750 | — | — |
| GIG–FCO (Roma, alternativa de entrada) | R$ 4.574 | — *(3 obs., 1 só ronda)* | R$ 4.731 | — | — |
| GIG–VCE (Veneza, alternativa de entrada) | R$ 4.606 | — *(3 obs., 1 só ronda)* | R$ 4.825 | — | — |
| CDG–GIG (Paris, referência p/ perna de volta) | R$ 3.147 *(ambíguo — pode ser só ida)* | — | R$ 5.243 | — | — |

*Uma observação por rota não é linha de base. Precisamos de ~5 rondas independentes (datas/horários de busca diferentes), colhidas ao longo de 2027, e nenhuma das rondas registradas até 2026-09-18 tem data de viagem confirmada em ago–set/2027 — todas são preço genérico "a partir de" capturado por buscador. Ver nota de falha em 2026-09-18 acima.*

## Gatilhos armados

Critérios pré-autorizados pelo Fabio. Quando um bate, o caçador monta o dossiê de execução e dispara alerta. Ver [[regras-de-compra]].

| # | Rota | Janela de datas | Pax | Teto por pessoa | Condições | Status |
|---|---|---|---|---|---|---|
| 1 | GIG→MXP · CDG→GIG (*open-jaw*) | **qualquer 12–15 dias entre 10/set e 15/out de 2028** | 3 | ~R$ 6.000 *(a calibrar)* | bagagem despachada inclusa; máx. 1 conexão; **preferência por saída ter/qua** | ⏸️ **aguardando abertura de vendas** |

> **Janela ampliada em 2026-09-01.** A família aderiu ao homeschooling e não tem calendário escolar.
> O gatilho deixou de ser uma data fixa e virou uma janela de cinco semanas com duração flexível.
> Isso multiplica as combinações avaliáveis — e é o número de combinações, não a sorte, que determina
> a chance de achar tarifa excepcional. Vale igualmente para disponibilidade de assento em resgate
> por milhas, que é escassa em data fixa e abundante em janela larga. Ver [[melhor-epoca]].

> **Por que o gatilho está pausado:** companhias vendem cerca de **330 dias à frente**. Passagens para
> setembro de 2028 só entram à venda por volta de **outubro de 2027** — não existe o que vigiar antes disso.
>
> **Plano até lá:** colher observações da mesma rota nas datas equivalentes de 2027 para montar a linha de
> base. Quando soubermos o que é preço normal em set/out, o teto deixa de ser chute e o gatilho é armado
> de verdade. Ver [[plano-de-viabilidade]].
