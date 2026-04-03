# Company Context: JPMorgan Chase Merchant Services

## Business Overview

**Entity:** JPMorgan Chase — Merchant Services division (part of CIB / Payments)
**Position:** One of the largest acquirers globally by volume
**Net Revenue:** ~$1.7B
**Profitability:** Operating near breakeven — a critical strategic tension
**Contrast:** Adyen operates at ~50% EBITDA margins on lower revenue. Gap = platform efficiency + pricing power.

---

## Strategic Position

### Strengths
- **Balance sheet & trust** — Enterprise merchants choose JPM for stability, counterparty risk tolerance, global banking relationships
- **Dual acquirer-issuer position** — Unique visibility into both sides of a transaction; powers Account Updater, IIAS, fraud intelligence
- **Issuer relationships** — Enables real-time account data, enhanced authorization rates
- **Healthcare / FSA / HSA** — `retailAddenda` and `healthcareData` object; genuine differentiator in regulated verticals
- **Global acquiring footprint** — Coverage that pure-play fintechs can't match for large multinationals

### Weaknesses
- **Developer experience** — API design, documentation, sandbox quality trail Stripe significantly
- **Platform debt** — Legacy architecture limits speed of feature delivery; modernization is a multi-year effort
- **Hosted UI** — Checkout.js / hosted payment page lags Stripe Elements / Payment Links in quality and flexibility
- **Agentic / AI commerce** — No clear strategy vs Stripe's LLM-native toolkits
- **Time to value for new merchants** — Onboarding and integration complexity higher than competitors

### Strategic Priorities
1. Platform modernization (API-first, event-driven, microservices)
2. Developer experience parity with Stripe
3. Margin improvement through automation and pricing intelligence
4. International expansion (EMEA particularly — Dublin as innovation hub)
5. AI/ML in authorization optimization, intelligent routing, fraud decisioning

---

## Revenue Model

- **Interchange-plus and flat-rate** pricing models
- **Value-added services** (vault, tokenization, authentication, account updater) as attach revenue
- **Net revenue** = gross processing revenue minus interchange, assessments, and operating costs
- Near-breakeven profile means every basis point of efficiency or VAS attach matters

---

## Org Context

- Transaction Processing (TP) is a platform org — serves internal product owners, solutions teams, and directly integrated enterprise merchants
- Platform vs. Solutions split is an active structural discussion: Platform builds the engine, Solutions handles go-to-market and merchant-facing delivery
- James does NOT own MOPS or Payment Brand initiatives — important for RACI clarity

---

## Key Tensions

| Tension | Detail |
|---------|--------|
| Speed vs. stability | Platform modernization at pace while maintaining 99.99%+ uptime |
| Platform vs. Solutions | Avoid PM fragmentation during transformation |
| Build vs. buy | Network tokenization (PULSE Side-by-Side), AU transformation |
| Cost discipline vs. investment | Near-breakeven limits discretionary spend |
