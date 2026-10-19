---
tipo: hot-cache
atualizado: 2026-10-19
janela_palavras: 302
limite: 500
---

# Hot Cache

Memória quente entre sessões. Lido logo depois do `CLAUDE.md` na abertura de toda sessão.

---

## Estado da Sessão

**O projeto:** levar Fabio (52), Fabiana (53) e Zoe (8, primeira viagem internacional) do Rio para **norte da Itália → Suíça → Disneyland Paris**. Cada um dos três queria um destino diferente; descobrimos que os três formam uma linha reta ([[rota-mestra]]).

**🎯 A data: setembro de 2028** — embarque alvo ~18/set. 24 meses de poupança de R$ 2.000/mês = R$ 48.000, contra custo realista de ~R$ 55.800. A diferença fecha com Livelo + parcelamento sem juros + gratuidades da Zoe na Suíça. Ver [[plano-de-viabilidade]].

**Por que setembro:** única janela que entrega os 7 critérios do Fabio — colheita de uva no Piemonte, sem calor, pouca chuva, neve garantida no alto (Jungfraujoch é geleira), poucas filas na Disney. E é mais barata que julho. Ver [[melhor-epoca]].

**Última operação:** `ingest` das decisões de 02/09 — duração fechada em **12–15 dias**, poupança de R$ 2.000/mês **confirmada**, teto de passagem delegado ao caçador. Tese do [[o-sonho]] está em **v1**, `confianca: media`.

**Preferências declaradas (o Fabio aceita sugestões):** Itália — Cinque Terre e Verona *fundamentais*, Piemonte *desejável*. Suíça — Jungfrau/Interlaken e Zermatt, trem cênico, pasto verde com neve ao fundo, escorregar na neve de trenó.

**Funcionários:** os 6 subagentes de `.claude/agents/` estão **ativos** (após reinício). Podem ser chamados pelo nome.

### ✅ Homeschooling — trava de calendário resolvida

A família aderiu ao homeschooling. Sem calendário escolar. Setembro/2028 confirmado, julho fora de cena.
Virou a **alavanca nº 6** do orçamento: janela de caça ampliada para 10/set–15/out, saída em meio de
semana, e — o que mais importa — muito mais chance de achar assento de resgate por milhas.

### ⏳ Dois agentes rodando (despachados 2026-09-02)

- ✅ `controlador-financeiro` → **ENTREGOU** `wiki/financeiro/estrategia-livelo.md`.
- ⏳ `curador-destinos` → **onde exatamente**. Ainda rodando. Entregáveis: páginas em `wiki/destinos/` + `wiki/consultas/onde-exatamente.md`.

### 💰 Livelo — o que ficou sabido (02/09)

**Correção contra o gerente:** os R$ 6.000 que eu estimei para a alavanca nº 1 **estavam errados**.
60.000 pontos hoje = **um trecho**, ~R$ 2.200–3.000. Com aporte de 24 meses, alvo realista **~R$ 5.000**
(fecha 64% dos R$ 7.800). Teto ~R$ 11.000 se as 6 pontas saírem por milhas.

- **Milhas anulam o prêmio de open-jaw** (~R$ 2.000): resgate são dois one-ways independentes.
  Se só uma ponta for de milhas, preferir **CDG→GIG** (Air France direto, taxa de resgate baixa).
- **O melhor programa para Europa dá o pior bônus:** LATAM resgata mais barato, bônus 25%;
  Smiles/Azul dão 80–100% mas cobram mais milhas. **Só decidir em out/2027**, com assentos na tela.
- **Alvo: 222.000 pontos** para as 6 pontas. Faltam ~162.000.
- **Transferir com bônus vale 2,3x** o Resgate Fácil (6,03 vs 2,60 c/ponto).

### 🔴 TAREFA DO FABIO — prazo 15/09/2026

**Abrir o extrato Livelo e anotar a data de vencimento de cada lote dos 60.000 pontos.**
Pontos expiram em 24 meses; a compra das passagens é jan–abr/2028 — parte pode virar pó antes.
Nenhuma fonte responde isso, só o extrato dele. Mitigação: Clube Livelo (pontos do assinante não
expiram) ou cartão cujos pontos não expiram (BB Altus, BRB Dux, Bradesco Aeternum).

### ✅ As duas tensões de 09-02 — RESOLVIDAS em 13/09/2026

Ambas fechadas por decisão do Fabio, ver [[onde-exatamente]] e [[decisao-paris]]: **Piemonte e Zermatt cortados**
(colheita de uva migra para o Valpolicella, 25 min de Verona; trenó da Zoe confirmado no Snow Fun Park do
Jungfraujoch, CHF 15, temporada até 18/out). Rota oficial: Arranjo A, **16 dias/15 noites**
([[decisao-16-dias]]). Esta seção ficou várias semanas desatualizada no hot cache — corrigida em 15/10/2026
durante a rotina do relatório mensal.

### Próximos trabalhos

1. **Grade fina do roteiro** (`arquiteto-roteiro`) — horários de RER C para Versalhes, reserva de entrada do
   Louvre, ainda não feita.
2. **Responder os dois itens vencidos da [[estrategia-livelo]]** (prazo 30/09/2026, sem registro de resposta):
   qual cartão a família usa para pontuar, e abrir 2ª conta Livelo para a Fabiana.
3. **Decisão sobre a vigilância de preços** — ver bloco de bloqueio de rede abaixo, pendente desde 20/09.
4. **Relatório mensal** (`concierge-visual`) — rotina mensal confirmada funcionando; 2º relatório publicado
   em 15/10/2026: https://claude.ai/artifact/CsHCdJtDq7hcBXJbkYSdm1

### Fatos que não podem ser esquecidos

- **Passagens de set/2028 são incotáveis hoje.** Cias vendem ~330 dias à frente → venda abre ~out/2027. Vigilância real começa lá; até então, colher linha de base nas datas equivalentes de 2027. Gatilho nº 1 já criado e **pausado** em [[historico-de-precos]].
- **Passagem *open-jaw*** (entra Milão, sai Paris) é a decisão de compra mais importante — economiza um dia inteiro e o trem de volta.
- **Passaportes ✅** válidos +5 anos. **ETIAS** é a mudança regulatória provável até 2028 — vigiar.
- **Eu não compro.** Ver [[regras-de-compra]]. Eu decido, o Fabio clica. Não reabrir sem ele pedir.
- Todos os custos são `[estimativa — não verificado]`, exceto os com fonte (KAYAK, myswissalps).

### Pendências operacionais

- Git não inicializado (recomendado; não commito sem pedido)
- Obsidian: Templates → `meta/templates/`; anexos → `raw/assets/`; instalar Dataview
- Vigilância automática via `/schedule` — só faz sentido a partir de out/2027

### 🚫 Coleta autônoma de preços — bloqueio de rede estrutural (confirmado 32x seguidas: 09-18 a 10-19, trinta e dois dias corridos)

O `cacador-ofertas` roda em agendamento autônomo diário, mas **`WebFetch` e `curl` direto estão
sistematicamente bloqueados** para qualquer domínio externo, não só sites de viagem — confirmado de
novo em 10-19 (`WebFetch` para KAYAK e Skyscanner devolveu `getaddrinfo ENOTFOUND` em ambos; `curl`
direto para kayak.com.br devolveu `CONNECT tunnel failed, response 403`).
O canal externo estável para abrir a issue de cada rodada continua sendo `gh api`/`gh issue create`
(REST). Só `WebSearch` funciona, e devolve snippets agregados/cacheados de baixíssima confiança (sem
data específica confirmada, 1 passageiro, sem bagagem) — **não serve para montar a linha de base real
de ago–set/2027**.
Achado de 10-19: Trip.com deu a primeira média mensal explícita para CDG-GIG favorável à premissa de
setembro barato (ainda sem ano confirmado); nenhum preço novo com confiança suficiente abaixo do teto;
nenhuma evidência de abertura de vendas para set/2028.
**Decisão do Fabio pendente desde 09-20, agora com 32 rodadas seguidas (vinte e nove dias corridos) sem
resposta:** (a) reduzir a frequência do agendamento, (b) montar alerta de tarifa nativo (Google
Flights/KAYAK, fora deste agente), ou (c) pedir liberação de egress para sites de passagem
especificamente. A reescalação direta mais recente foi em 10-17 (marco de um mês corrido); esta rodada
(10-19) não repetiu a escalação, apenas registrou a espera.
Detalhe completo em [[historico-de-precos]], nota de 2026-10-19.

**Pendência de manutenção (desde 10-14, ainda não resolvida):** [[historico-de-precos]] passou de 650
linhas (agora ~790), acima do limite de ~400 linhas recomendado pelo `CLAUDE.md` §2 — considerar
arquivar rodadas mais antigas em sub-página numa próxima sessão com o Fabio no circuito (fora do
escopo de uma coleta diária autônoma).

---

## Janela Literal — últimas 500 palavras do Fabio

Texto verbatim, mais antigo em cima. Ao estourar 500 palavras, corto do topo; antes de cortar, promovo qualquer decisão durável para o `CLAUDE.md` ou para a wiki.

### [2026-09-01] turnos 1–2
*(cortados: artigo LLM Wiki → `raw/2026-09-01-llm-wiki-padrao.md`; regras do método → `CLAUDE.md` §1–§8; briefing da agência → `raw/2026-09-01-briefing-fundador.md` e `CLAUDE.md` §9)*

### [2026-09-01] turno 3 — briefing completo

> Viajaremos, Eu, Fabio, 52 anos, Minha esposa Fabiana de 53 e nossa caçula, Zoe de 8, em sua primeira viagem internacional.
> Minha esposa quer o norte da italia eu a suiça, e a Zoe, a Eurodisney,
> Saimos do Rio de Janeiro
> Considere que guardo 2mil reais por mês
> A Janela, voce vai me sugerir a melhor época, que nos possibilite não sentir tanto rio, nem tanto calor, que tenha eventos interessantes como colheita de uvas, algum festival tradicional interessante, paisagens belas, neve no alto da montanha para poucas filas nas atrações,
> Duração de 10 a 15 dias
> Prazo emocional, Entre segundo semestre de 27 e primeiro de 29
> Sim, PAssaportes válidos por mais 5 anos
> Tenho por volta de 60 mil pontos hoje no livelo
> ainda não tenho eto absoluto
> mas considere que viajamos de economica, podemos ficar em Apartamentos airbnb, ou hoteis de 3 ou 3 estrelas com notas acima de 8 nos sites especializados. Dentro da Europa, preferimos o trem, mas se compensar, podemos locar automovel.

### [2026-09-01] turno 4

> Noss familia aderiu ao HomeScholing com a Zoe, assim, temos fexibilidade necessária
> Sim, quero dicas com o controlador financeiro

### [2026-09-01] turno 5

> os 6 funcionarios já estão ativos?
> quais decisões estao em aberto?

### [2026-09-02] turno 6 — decisões sobre Itália e Suíça

> 1 - Sim, refaça Livelo
> 2 - Cinque Terre e Verona são fundamentais., A colheita em piemonte desejavel
> 3 - JUngfrau Interlaken e Zermatti, Passeio de trem pelos alpes, quero vistas belas com pastos verde e neve ao fundo. Uma experiencia de escorregar na neve, com um  treno
> 4 - duração entre 12 e 15 dias
> 5 - Melhor custo beneficio, é traalho do caçador de ofertas
> 6 - Confirmado
>
> Para a 2 e 3, ainda quero o trabalho do curador-destinos, o que eu coloquei é uma primeira ideia, mas aceito sugestões
