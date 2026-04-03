# Skill: Opportunity Assessment

## When to Use
Quickly evaluating whether an idea, request, or market signal is worth pursuing. Use before committing to a PRD. Good for: executive questions, inbound merchant requests, competitive signals, team proposals.

## Inputs Required
- Opportunity description (can be rough)
- Source (merchant request, competitive intel, internal proposal, regulatory requirement)

## Instructions for Claude

Load `context/company.md`, `context/product.md`, `context/competitors.md`.

---

### Output Structure (Keep It Tight — 1 Page)

#### The Opportunity in One Sentence
What is this, really?

#### Why Now?
What makes this timely? (Regulatory window, competitive pressure, merchant demand signal, technology unlock)

#### Who Benefits?
Merchant segments. Internal stakeholders. Revenue impact.

#### Desirability / Viability / Feasibility

| Lens | Assessment | Evidence |
|------|-----------|----------|
| Desirability | H/M/L | Is there real merchant demand? |
| Viability | H/M/L | Does it improve revenue, margin, or retention? |
| Feasibility | H/M/L | Can TP platform support this? What's the build complexity? |

#### Competitive Dimension
Does this close a gap vs. Stripe/Adyen, or extend a JPM advantage?

#### Recommended Next Step
One of: Deprioritize / Monitor / Spike / Add to roadmap / Escalate for investment

#### Open Questions Before Proceeding
What do we need to know before committing?

---

## Output Format
Save to `/artifacts/OpportunityAssessment-[topic]-[YYYY-MM-DD].md`
