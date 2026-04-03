# Product Context: Transaction Processing Platform

## Platform Scope

James owns product for the full Transaction Processing (TP) platform:

### Front-End
- **APIs** — Authorization, capture, void, refund; the primary merchant-facing interface
- **Orchestration** — Routing logic, retry strategies, network selection
- **Value-Added Services:**
  - Payment Credential Vault (PCI DSS Level 1, NTK, revelation proxy)
  - Authentication Platform (3DS, VDCAP, SCA/PSD2)
  - BIN/Routing intelligence

### Back-End
- **Settlement** — Multi-network, multi-currency, multi-entity
- **Pricing & Billing** — Interchange-plus, flat-rate, fee schedules
- **Reconciliation** — Merchant-facing recon, internal GL reconciliation, break management

---

## Key Product Areas & Direct Report Ownership

| Area | Lead | Key Initiatives |
|------|------|-----------------|
| Payments & Services | Khalid Ghori | Authorization optimization, OCT/instant refunds |
| Monetization & Settlement | Kari Hytoenen | Single Payout & Pricing Initiative, settlement modernization |
| Financial Accounting & Recon | Dhaval Shah | EU MOP Recon, AI/ML break management, debit recon automation |
| CARe & Migrations | Dawn Gillooly | Customer migration tooling, CARe platform |
| Validations & Intelligence | Varun Munjal | Fraud decisioning, intelligent routing, ML models |
| Product Architecture | Josh Moushon | Platform architecture, API design standards, ARB |

---

## Active Initiatives (Detailed)

### Payment Credential Vault (Priority: P0)
- PRD v1.3 complete — 92 prioritized requirements (48 P0, 31 P1, 13 P2)
- Seven bounded contexts: credential storage, network tokenization, account updater, revelation proxy, BIN enrichment, audit/compliance, admin/lifecycle
- Network tokenization covers: Visa (VTS), Mastercard (MDES), Amex, Discover (all at P0)
- ARB-ready architecture document + OpenAPI 3.0 spec (36 operations, 7 API groups)
- Key domain terms: NTK, AU, RTAU, TRID, PAR, VTS, MDES, SAQ-A/SAQ-D, HSM, AES-256-GCM, revelation proxy, BIN enrichment, Safetech

### IIAS / Healthcare Payments (Priority: Strategic Differentiator)
- `retailAddenda` + `healthcareData` object — JPM's genuine moat in healthcare acquiring
- IIAS = Inventory Information Approval System (FSA/HSA card eligibility at item level)
- PINless debit routing defect recently surfaced — root cause analysis and remediation in progress
- Stripe and Adyen have minimal healthcare-specific capability here

### VDCAP / SCA / PSD2
- VDCAP requires 3DS data-only flows or network token cryptogram requests (not simple auth enrichment)
- Active build — Europe regulatory requirement
- TRA fraud rate monitoring, cumulative limit tracking, 3DS adoption rates, frictionless flows

### Reconciliation Modernization
- Two swim lanes:
  1. **Feature Launch & Product Expansion** — EU MOP Recon tranches, debit recon automation
  2. **Platform Support & Modernization** — Single Payout & Pricing Initiative, Backend Modernization
- AI/ML break management is a roadmap initiative

### Account Updater Transformation
- Three horizons:
  1. File-based AU modernization (current)
  2. API-first tokenization bundles
  3. AI-powered payment intelligence (long-term)
- Competitive lever: JPM's dual acquirer-issuer position enables higher match rates than pure-play AU vendors

### Debit Routing / OCT
- Visa OCT/faster refunds complexity: original purchases may route through PIN networks (STAR, NYCE, PULSE); OCT refunds return via Visa Direct
- Goal: network-agnostic instant refund capability, not simple Visa product adoption
- PULSE Side-by-Side Token Service being evaluated as build/partner option

---

## Platform Architecture Principles

- API-first design (OpenAPI 3.0 standard)
- Event-driven where possible
- Domain-driven design — bounded contexts per PRD v1.3 model
- PCI DSS compliance as a baseline constraint, not a feature
- HSM for all key operations; AES-256-GCM for data at rest

---

## Product Metrics That Matter

| Metric | Why It Matters |
|--------|---------------|
| Authorization rate | Directly impacts merchant revenue; +10bps = meaningful GMV at scale |
| Vault attachment rate | VAS revenue lever |
| Reconciliation break rate | Operational cost driver; AI/ML can attack this |
| Time to integration | Developer experience proxy; Stripe advantage here |
| Network token adoption | Reduces fraud, improves auth rates, enables AU |
| 3DS frictionless rate | SCA compliance without checkout conversion drag |
