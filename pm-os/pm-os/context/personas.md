# Stakeholder Personas

## Internal Stakeholders

### Engineering Lead / Platform Architect
**Cares about:** Technical feasibility, architecture integrity, avoiding rework, migration complexity, PCI scope
**Pushes back on:** Vague requirements, underspecified APIs, scope creep mid-sprint
**Speaks in:** System design terms, capacity, toil, tech debt ratios
**Win with:** Detailed specs (Gherkin, OpenAPI), clear bounded contexts, migration paths defined upfront

### Sales / Solutions
**Cares about:** Merchant win rates, competitive displacement, deal velocity, pricing clarity
**Pushes back on:** Features that don't have a merchant story, gaps vs. Stripe in the sales cycle
**Speaks in:** Win/loss data, ACV, merchant verticals, deal stages
**Win with:** Clear competitive differentiation, customer-ready narratives, early previews of new capabilities

### Finance / CFO Proxy
**Cares about:** Revenue impact, cost discipline, investment payback, margin improvement
**Pushes back on:** Vague ROI, investment asks without clear returns, scope that grows silently
**Speaks in:** Basis points, net revenue, operating leverage
**Win with:** Business case with conservative/base/upside scenarios; attach rate models

### Executive / Head of Merchant Services
**Cares about:** Strategic alignment with banking relationship, EBITDA trajectory, enterprise merchant retention, regulatory posture
**Pushes back on:** Platform investment that doesn't connect to merchant growth or margin
**Speaks in:** Market share, NPS, regulatory risk, investor narrative
**Win with:** Competitive urgency framing, healthcare/regulated vertical differentiation, clear platform modernization milestones

---

## External: Merchant Personas

### Enterprise Merchant (Regulated / Healthcare)
**Example:** Large hospital network, FSA-heavy retailer
**Cares about:** IIAS accuracy, FSA/HSA card acceptance, compliance posture, stability
**JPM advantage:** `retailAddenda` + `healthcareData`; IIAS certification
**Pain points:** Integration complexity, slow onboarding

### Enterprise Merchant (Global / Multinational)
**Example:** Global retailer, SaaS platform, marketplace
**Cares about:** Global acquiring coverage, unified settlement, FX, one banking relationship
**JPM advantage:** Full banking + acquiring bundle
**Pain points:** API quality vs. Stripe, hosted UI limitations

### Developer / Technical Integrator
**Example:** Head of Payments Engineering at a mid-market SaaS
**Cares about:** API quality, documentation, sandbox, time to first successful transaction
**JPM gap:** DX lags Stripe meaningfully
**What would win them:** API parity + honest roadmap + responsive support

### Platform / Marketplace
**Example:** SaaS platform with embedded payments for sub-merchants
**Cares about:** Sub-merchant onboarding, split settlement, compliance offload
**JPM gap:** No native platform/marketplace product equivalent to Stripe Connect
