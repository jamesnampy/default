# Skill: Roadmap Planning

## When to Use
Building or refining a product roadmap for a capability area, planning cycle, or executive presentation.

## Inputs Required
- Scope: which product area(s)?
- Horizon: quarterly / annual / 3-year
- Constraints: engineering capacity, regulatory deadlines, strategic mandates
- Format: narrative / swim-lane / table / exec deck

## Instructions for Claude

Load `context/product.md`, `context/company.md`, and relevant team context.

---

### Output Structure

#### 1. Strategic Context
Why does this roadmap exist? What's the business problem or opportunity it addresses?
One paragraph. Reference company priorities.

#### 2. Themes
3-5 overarching themes that organize the roadmap (not feature lists).
Example themes: "Platform Modernization", "Developer Experience Parity", "VAS Revenue Expansion"

#### 3. Roadmap by Horizon

**Now (0-3 months) — Commit**
| Initiative | Theme | Value | Owner | Status |
|-----------|-------|-------|-------|--------|
| ... | ... | ... | ... | In flight / Starting |

**Next (3-6 months) — Plan**
| Initiative | Theme | Value | Owner | Dependencies |
|-----------|-------|-------|-------|--------------|
| ... | ... | ... | ... | ... |

**Later (6-18 months) — Explore**
| Initiative | Theme | Value | Confidence | Open Questions |
|-----------|-------|-------|-----------|----------------|
| ... | ... | ... | H/M/L | ... |

#### 4. Deliberate Deprioritizations
What are we NOT doing, and why? This builds trust and prevents scope creep.

#### 5. Key Dependencies & Risks
What could break this roadmap? Engineering capacity, regulatory changes, platform dependencies.

#### 6. Success Metrics
How will we know this roadmap delivered value?

---

## Roadmap Design Principles for TP

- Reconciliation roadmap: maintain two swim lanes (Feature Launch & Platform Support/Modernization)
- Always distinguish regulatory/compliance work from discretionary product work
- Flag MOPS and Payment Brand dependencies — these are cross-team, not TP-owned
- Every "Later" item needs at least one open question documented (this is what makes it honest)

## Output Format
Save to `/artifacts/Roadmap-[area]-[YYYY-MM-DD].md`
