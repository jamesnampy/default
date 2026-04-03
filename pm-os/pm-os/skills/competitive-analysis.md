# Skill: Competitive Analysis

## When to Use
Analyzing a specific capability, feature area, or market position against Stripe and/or Adyen. Useful for: executive briefings, PRD context sections, roadmap prioritization, sales enablement.

## Inputs Required
- Capability or feature area to analyze (e.g., "hosted checkout", "network tokenization", "developer onboarding")
- Depth: Quick (2-3 pages) / Standard (full briefing) / Deep (with API-level analysis)

## Instructions for Claude

Load `context/competitors.md` and `context/product.md`.

---

### Output Structure

#### 1. Executive Summary (3-5 bullets)
The most important things to know. Decision-ready.

#### 2. Capability Matrix

| Capability | JPMorgan MS | Stripe | Adyen | Notes |
|-----------|-------------|--------|-------|-------|
| [Sub-capability 1] | ✅ / ⚠️ / ❌ | ... | ... | ... |
| [Sub-capability 2] | ... | ... | ... | ... |

Legend: ✅ Strong  ⚠️ Partial / in progress  ❌ Gap / absent

#### 3. JPM Advantages
Where JPM genuinely wins. Be honest — don't inflate.

#### 4. JPM Gaps
Where JPM trails meaningfully. Prioritize by merchant impact.

#### 5. Competitive Risk Assessment
| Gap | Risk Level | Merchant Segment Impacted | Urgency |
|-----|-----------|--------------------------|---------|
| ... | H/M/L | ... | Now / 6mo / 12mo+ |

#### 6. Recommended Actions
What should TP do as a result of this analysis?
Tie to existing roadmap initiatives where possible.

#### 7. Sources & Confidence
Note which findings are from primary research, public documentation, or inference.

---

## Output Format
Save to `/artifacts/CompetitiveAnalysis-[topic]-[YYYY-MM-DD].md`
