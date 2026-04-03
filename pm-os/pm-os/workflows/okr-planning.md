# Workflow: OKR Planning Cycle

## Purpose
Run a full OKR planning cycle for a product area or the full TP platform in 1-2 focused sessions.

## Steps

---

### Step 1: Strategic Input Gathering
**Prompt:** "Help me prepare for OKR planning for [area / full TP]."

Claude will:
- Load `context/company.md`, `context/product.md`, `context/team.md`
- Summarize active initiatives and their current status
- Surface the top 3-5 strategic priorities for the cycle
- Identify any RACI gaps or cross-team dependencies to flag

---

### Step 2: Draft Objectives
**Prompt:** "Draft 3-5 objectives for [area] for [quarter/year]."

Claude will:
- Produce qualitative, inspiring objectives
- Tag each as: Platform Modernization / Revenue Growth / Operational Excellence / Compliance
- Check for balance across these categories

---

### Step 3: Key Results per Objective
**Prompt:** "Write Key Results for Objective [N]."

Claude will:
- Load `skills/okrs.md`
- Produce 3-4 measurable KRs per objective
- Apply the two-layer framework (direct ownership vs. cross-functional influence)
- Flag baseline data needed

---

### Step 4: Quality Check
**Prompt:** "Run the quality check on these OKRs."

Claude will check each KR against:
- Is it an outcome, not an output?
- Is the baseline known?
- Is there a single clear owner?
- Is the accountability layer correctly classified?
- Are network mandate compliance items flagged?

---

### Step 5: Combined Deck Assembly
**Prompt:** "Format these as a combined OKR summary for the townhall deck."

Claude will produce:
- Color-coded ownership table (James's area vs. peer areas)
- RACI gap analysis
- Individual product area slides in formal, outcome-oriented style
- Executive summary slide

---

## Notes from Prior Cycle
- 34 KRs combined deck completed with color-coded ownership
- Key RACI gap: network mandate compliance ownership between TP and Payment Brand
- Style: formal, outcome-oriented — not activity lists
