# Skill: OKR Planning

## When to Use
Setting or refining OKRs for a product area, planning cycle, or team. Also for reviewing existing OKRs for quality and measurability.

## Inputs Required
- Product area or initiative
- Planning horizon (quarterly / annual)
- Strategic priorities to align with (or load from `context/company.md`)
- Existing draft OKRs (optional — will generate from scratch if not provided)

## Instructions for Claude

Load `context/company.md`, `context/product.md`, and `context/team.md`.

Apply James's two-layer accountability framework:
- **Direct ownership OKRs** — James/TP team is accountable
- **Cross-functional influence OKRs** — TP contributes but doesn't own the outcome

---

### Output Structure

#### Objective [1-3 per area]
*Qualitative, inspiring, directional. Should answer: what are we trying to achieve and why does it matter?*

**Key Result 1:** [Measurable outcome — not an activity]
- Baseline: [current state]
- Target: [specific number/threshold]
- Owner: [direct report name]
- Accountability layer: Direct / Influence

**Key Result 2:** ...

**Key Result 3:** ...

---

### Quality Checks (Apply to Each KR)
- [ ] Is it an outcome, not an output? ("authorization rate +50bps" not "launch auth optimization feature")
- [ ] Is the baseline known or estimable?
- [ ] Is the target ambitious but achievable (70% confidence)?
- [ ] Is there a single clear owner?
- [ ] Is the accountability layer correctly classified?
- [ ] Is it free of vanity metrics?

### RACI Gap Check
After drafting, flag any KRs where:
- Network mandate compliance is involved (historically a RACI gap)
- Cross-team dependency is required but no DRI is named
- MOPS or Payment Brand work is implicated (out of scope — flag and redirect)

---

## Output Format
Save to `/artifacts/OKRs-[area]-[YYYY-MM-DD].md`
