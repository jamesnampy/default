# Workflow: Discovery → PRD

## Purpose
Turn raw customer feedback, research, or a problem signal into a structured PRD ready for engineering review.

## Steps

---

### Step 1: Problem Framing
**Prompt:** "I have [input: feedback / research / problem signal]. Help me frame the problem."

Claude will:
- Identify the core job to be done (load `skills/jtbd.md`)
- Separate symptoms from root causes
- Identify the merchant segment most affected
- Draft a crisp problem statement (2-3 sentences)

**Output:** Problem statement + JTBD analysis saved to `/artifacts/`

---

### Step 2: Opportunity Assessment
**Prompt:** "Now run an opportunity assessment on this problem."

Claude will:
- Load `skills/opportunity-assessment.md`
- Score desirability / viability / feasibility
- Identify competitive dimension (load `context/competitors.md`)
- Recommend next step: proceed / spike / deprioritize

**Output:** Opportunity assessment saved to `/artifacts/`

---

### Step 3: Solution Exploration
**Prompt:** "Generate 3 solution approaches for this problem."

Claude will:
- Produce 3 distinct approaches (not just variations of one)
- For each: brief description, tradeoffs, estimated complexity (S/M/L/XL)
- Flag which aligns best with platform architecture

**Output:** Solution options doc saved to `/artifacts/`

---

### Step 4: PRD Draft
**Prompt:** "Write the PRD for [chosen solution approach]."

Claude will:
- Load `skills/prd.md`
- Generate full structured PRD
- Apply all quality checks (Gherkin for P0s, explicit non-goals, measurable metrics)

**Output:** PRD saved to `/artifacts/PRD-[name]-[date].md`

---

### Step 5: Sub-Agent Review
**Prompt:** "Run CTO and Devil's Advocate reviews on this PRD."

Claude will:
- Load `agents/cto.md` and `agents/ux-user-devil.md`
- Produce structured reviews from each agent
- Consolidate a "top 5 things to fix" list

**Output:** Review notes saved to `/artifacts/`

---

### Step 6: PRD Refinement
**Prompt:** "Update the PRD based on the review feedback."

Claude will apply review feedback and produce PRD v2.

---

## Total Time Estimate
- With good input: 45-90 minutes end to end
- Starting from scratch: 2-3 hours

## Data Inputs That Accelerate This Workflow
Drop into `/data/input/` before starting:
- Customer interview transcripts
- Support ticket summaries
- Survey results
- Competitive research
- Engineering spike notes
