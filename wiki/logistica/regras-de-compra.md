---
tipo: conceito
titulo: Regras de Compra — o que eu posso e o que eu não posso fazer
criado: 2026-09-01
atualizado: 2026-09-01
tags: [logistica, compra, limite, protocolo]
fontes: ["[[briefing-fundador]]"]
confianca: alta
status: ativo
---

# Regras de Compra — o que eu posso e o que eu não posso fazer

> **Eu não compro passagem.** Não tenho cartão, não tenho login em site de companhia aérea, e não executo pagamento sozinho. Isso não é timidez de configuração — é o desenho certo para dinheiro de família.

Esta página existe porque o [[briefing-fundador]] pediu "ser capaz de acessar e comprar quando surgirem ofertas incríveis". Metade disso é viável hoje. A outra metade não é, e é melhor você saber disso agora do que numa madrugada de promoção relâmpago.

## O que eu não faço

| Pedido | Situação | Por quê |
|---|---|---|
| Digitar seu cartão num checkout | **Não** | Não tenho suas credenciais e não vou pedir por elas |
| Comprar sozinho enquanto você dorme | **Não** | Compra é irreversível, cara e sujeita a taxa de cancelamento. Ação assim tem que ter um humano no gatilho |
| Logar na sua conta de milhas | **Não** | Mesma coisa |

Um erro meu numa busca custa cinco minutos. Um erro meu num checkout custa passagem de família inteira, com multa pra desfazer. A assimetria decide.

## O que eu faço — e resolve 95% do problema

O gargalo de uma promoção relâmpago não é o ato de pagar. **É a decisão.** Quando a tarifa cai às 2h da manhã, o que faz a família perder a oferta é não saber se aquele preço é bom, se a data serve, se o orçamento aguenta, quais assentos, qual bagagem. Isso tudo eu posso ter pronto **antes**.

**1. Vigilância.** Monitoro rotas e datas em ciclo recorrente (via tarefa agendada de verdade — `/schedule` ou `/loop`). Registro cada preço visto em [[historico-de-precos]], para a gente saber o que é oferta e o que é preço normal disfarçado de oferta.

**2. Gatilho pré-autorizado.** Você define antes, com calma, os critérios. Algo como:

> *Voo GRU→destino, ida entre 10 e 25 de julho, volta 12–18 dias depois, 4 pessoas, bagagem despachada inclusa, no máximo 1 conexão, até R$ X por pessoa → **dispara**.*

Isso vira um arquivo em `wiki/ofertas/`. Quando bater, eu não pergunto "achei uma passagem, que acha?". Eu entrego um **dossiê de execução**.

**3. Dossiê de execução.** O pacote que transforma 40 minutos de pesquisa nervosa em 3 minutos de digitação:

- link direto do resultado da busca
- preço por pessoa e total, com taxas
- comparação com os últimos 30 dias de preço daquela rota — *isto é oferta ou é ruído?*
- o que essa compra faz com o orçamento ([[plano-de-viabilidade]])
- regra de bagagem, remarcação e cancelamento
- prazo estimado de validade da tarifa
- **veredito:** compra, espera, ou passa — com o motivo

**4. Alerta que te acorda.** Notificação push no seu aparelho quando o gatilho bater, não uma mensagem esperando você abrir o chat.

**5. Acompanhamento pós-compra.** Você compra, me manda o comprovante, eu filo em `raw/`, atualizo orçamento, roteiro e prazos.

## A divisão, em uma linha

**Eu decido. Você clica.** Eu carrego todo o peso analítico; você mantém a última palavra sobre o seu dinheiro.

## Exceção que vale discutir depois

Se em algum momento você quiser automação real de compra, o caminho honesto não sou eu com seu cartão — é um alerta de tarifa nativo (Google Flights, Kayak) rodando **junto** comigo, com a compra saindo do app oficial. Eu faço a análise, o app faz o clique. Podemos montar isso quando os gatilhos estiverem definidos.

## Relacionadas

- [[plano-de-viabilidade]] — o teto que define o que é "oferta incrível"
- [[historico-de-precos]] — a base que separa oferta real de marketing
- [[o-sonho]] — o que estamos comprando, afinal
