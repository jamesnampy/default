# Skill: Jobs to Be Done (JTBD) Analysis

## When to Use
Reframing a feature request, validating a problem space, building a discovery brief, or creating user stories grounded in real motivation rather than surface behavior.

## Inputs Required
- Feature or initiative to analyze
- Target user segment (optional — will default to relevant merchant personas)

## Instructions for Claude

Load `context/personas.md` and `context/product.md`.

Structure the output as follows:

---

### 1. Core Job Statement
**When** [situation/trigger]
**I want to** [motivation — what they're trying to accomplish]
**So I can** [desired outcome — functional, emotional, or social]

### 2. Job Map (Steps in the Job)
Break the job into 8 phases:
1. **Define** — What does the user need to figure out first?
2. **Locate** — What inputs/resources do they need to find?
3. **Prepare** — What setup is required?
4. **Confirm** — What do they check before proceeding?
5. **Execute** — The core action
6. **Monitor** — How do they track progress/outcomes?
7. **Modify** — What adjustments might they need to make?
8. **Conclude** — How does the job end / what does success look like?

### 3. Underserved Outcomes
For each job step, identify:
- What desired outcome is currently unmet or poorly served?
- Opportunity score framing: importance vs. satisfaction

### 4. Competing Solutions
What are users doing TODAY to get this job done? (Workarounds, competitors, manual processes)

### 5. Product Implications
What features, capabilities, or changes would best serve this job?
Map to P0/P1/P2.

---

## Output Format
Save to `/artifacts/JTBD-[topic]-[YYYY-MM-DD].md`
