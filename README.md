# Finvestimento — v1.3

**Finvestimento** é um app estático para controle de patrimônio, cálculo de IR/IOF (2025), simuladores e **importação Clear**, com **autocomplete de tickers da B3** e **cotação instantânea** via **brapi.dev**.

## Recursos
- **Transações**: compras/vendas, aportes, rendimentos; importação **Clear** (CSV/XLSX).
- **Impostos**: **compensação de prejuízos** mês a mês (ações comuns, day trade, FIIs, ETFs) e abatimento de IRRF.
- **Simulador**: CDB, Tesouro Selic/Prefixado, **CRI/CRA (isentos)**, **IPCA+ com cupons**, **Debêntures não‑incentivadas**, **ETF de RF** (sem come‑cotas), FIIs, ações.
- **Cotações**: autocomplete + preço atual usando **brapi.dev** (recomenda-se **Proxy** para proteger o token).

## Publicação (GitHub Pages)
1. Suba estes arquivos em um repositório (ex.: `finvestimento`).
2. Em **Settings → Pages**, selecione *Deploy from a branch* (main / root).
3. Acesse a URL do Pages.

## Configuração de cotações (brapi.dev)
- Em **Config.**, informe seu **token brapi.dev** (para autocomplete e cotações). **Evite expor o token** em produção — prefira configurar um **Proxy** (Cloudflare Worker/Vercel) que injete o token no backend.
- Endpoints usados: `/api/quote/list?search=...&type=stock` (busca), `/api/quote/{TICKER}` (cotação).

> Este app é apenas de apoio e não substitui orientação contábil.
