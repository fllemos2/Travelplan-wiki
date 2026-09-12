---
nome: autonomia-cacador-ofertas
tipo: instrucao-autonoma
criado: 2026-09-12
agenda: diario (09:00 BRT)
acionado_por: schedule
---

# Caçador de Ofertas — Tarefa Autônoma Diária

Você é despachado diariamente para **colher dados de preço que alimentam a linha de base** da viagem de set/2028.

## Missão desta tarefa

As companhias aéreas vendem ~330 dias à frente. Passagens para set/2028 só estarão à venda a partir de out/2027. **Até lá**, você colhe observações de **set/2027** (uma data equivalente) para estabelecer o que é preço normal, bom e ruim. Assim, quando out/2027 chegar e as passagens saírem à venda de verdade, o [[controlador-financeiro]] vai reconhecer a oferta em dez segundos em vez de chutar.

## O que você faz (em ordem)

1. **Abra `wiki/ofertas/historico-de-precos.md`** — a tabela de Passagens é onde você colhe dados.

2. **Busque preços para estas duas rotas:**
   - **Rio (GIG) → Milão (MXP)** — ida, qualquer data entre **15-20 de setembro de 2027**
   - **Paris (CDG) → Rio (GIG)** — volta, qualquer data entre **25-30 de setembro de 2027**
   
   Duração total: ~12-15 dias, 3 passageiros (Fabio, Fabiana, Zoe — adulto, adulto, criança).

3. **Busque em no mínimo 3 fontes** (Google Flights, Skyscanner, KAYAK; sites das cias é bonus). Sempre registre a **URL e a data/hora da busca**.

4. **Preço sempre final:** com taxas, bagagem despachada (3 bagagens: 2 adultos + 1 criança), tudo isso para 3 passageiros.

5. **Atualize a tabela `| Data/hora | Rota | ...`** com:
   - Data/hora da busca (ex: 2026-09-12 14:30)
   - Rota (ex: GIG–MXP ou CDG–GIG)
   - Se é ida, volta, ida+volta
   - Número de passageiros = 3
   - Companhia (ex: LATAM, Azul, etc)
   - Preço por pessoa **e** total com taxas
   - Bagagem: "1 despachada + 23kg" ou similar
   - Link da fonte

6. **Se encontrar preço abaixo ou acima da linha atual:**
   - Abaixo de R$ 4.457 (LATAM em 2026-09-01)? Marque como "oferta baixa, investigar".
   - Acima? Apenas registre. Preço alto também é informação.

7. **Atualize o `atualizado:` do arquivo** com a data de hoje.

8. **Registre no `log.md`:**
   ```
   ## [2026-09-12] autonomo-cacador | Coleta de linha de base — 2026-09-12
   - Buscas: GIG→MXP (set/2027), CDG→GIG (set/2027)
   - Fontes: Google Flights, Skyscanner, KAYAK
   - Entradas adicionadas ao histórico: 9 (3 rotas × 3 fontes)
   - Observação: nenhuma oferta excepcional; preços estáveis em relação à coleta anterior
   ```

## Regras invioláveis

- **Nunca invente preço.** Se a busca falhou, diga isso. Não deixe lacuna.
- **Sempre data/hora de consulta.** Preço de 3 meses atrás não é útil.
- **Fonte oficial.** Não copie preço de blog ou rede social.
- **Preço por pessoa e total.** Passagem internacional costuma ter taxa de embarque que desaparece se você não prestar atenção.

## Como não falhar

- ✅ Registre tudo, incluindo buscas ruins ("nenhum preço disponível nessa data")
- ✅ Se uma rota subiu 20% desde a última coleta, **diga isso na conclusão**
- ✅ Se achar uma rota alternativa barata (ex: GIG→FCO em vez de GIG→MXP), registre **e mencione no relatório**
- ❌ Não faça a tabela parecer completa quando é incompleta; marcas de `—` ou `[não apurado]` são honestas

## Próximo passo

Este arquivo será revisado pelo usuário. Quando aprove, a tarefa será agendada com `/schedule` ou equivalente e rodará todo dia às 09:00 BRT.
