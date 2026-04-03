# PM Operating System: Build Guide
### James's Claude Code OS for Transaction Processing Product Work

---

## What You're Building

A Claude Code-powered PM OS that:
- **Remembers everything** across every session — no re-explaining your business
- **Runs PM frameworks** (PRD, JTBD, OKRs, competitive analysis) in minutes
- **Pressure-tests your work** through 6 personalized sub-agents before it reaches stakeholders
- **Gets better over time** as you maintain and evolve it

This guide walks you through setup, usage, and the 30-day habit plan to make it stick.

---

## How It Works: The Core Mechanic

Claude Code automatically reads `CLAUDE.md` at the start of **every session**. This is your persistence layer.

```
Every session starts:
Claude Code opens → reads CLAUDE.md → loads context files → you're productive in 30 seconds
```

No more re-explaining that you're Co-Head of TP at JPMorgan. No more re-explaining the Vault initiative. No more pasting in competitor context. It's just there.

---

## File Structure

```
pm-os/
├── CLAUDE.md                        ← Claude Code reads this automatically every session
│
├── context/                         ← Persistent knowledge base
│   ├── company.md                   ← JPMorgan MS: business model, strategy, financials
│   ├── product.md                   ← TP Platform: scope, initiatives, metrics
│   ├── team.md                      ← Direct reports, peers, org dynamics
│   ├── competitors.md               ← Stripe & Adyen: positioning, gaps, advantages
│   └── personas.md                  ← Internal stakeholders & merchant segments
│
├── skills/                          ← Reusable PM frameworks
│   ├── prd.md                       ← PRD structure + quality checks
│   ├── jtbd.md                      ← Jobs to Be Done analysis
│   ├── okrs.md                      ← OKR planning with two-layer accountability
│   ├── competitive-analysis.md      ← Capability matrix + action recommendations
│   ├── roadmap.md                   ← Roadmap planning with swim lanes
│   ├── opportunity-assessment.md    ← Quick viability scoring
│   └── prfaq.md                     ← Working backwards from the press release
│
├── agents/                          ← Sub-agent reviewers
│   ├── cto.md                       ← Engineering feasibility, architecture, PCI
│   ├── executive.md                 ← Business case, strategic alignment, funding
│   ├── sales.md                     ← Competitive displacement, merchant story
│   └── ux-user-devil.md             ← UX, User Advocate, Devil's Advocate (3-in-1)
│
├── workflows/                       ← Multi-step processes
│   ├── discovery-to-prd.md          ← Problem signal → reviewed PRD
│   └── okr-planning.md              ← Full OKR cycle in one session
│
├── data/
│   └── input/                       ← Drop research, transcripts, reports here
│
└── artifacts/                       ← All outputs saved here (datestamped)
```

---

## Setup Instructions

### Step 1: Install Claude Code
```bash
npm install -g @anthropic-ai/claude-code
```
Requires Node.js 18+. Runs in your terminal.

### Step 2: Set Up Your Project Directory
```bash
# Clone or download the pm-os folder
cd ~/pm-os

# Start Claude Code from this directory — CLAUDE.md is loaded automatically
claude
```

**That's it.** Claude Code sees `CLAUDE.md` and loads your context. You're ready.

### Step 3: Verify Context Is Loaded
First session, say:
> "Summarize what you know about my product scope and current priorities."

You should get back a tight summary of TP, the Vault initiative, and your competitive position — without having told Claude anything.

---

## How to Use Each Component

### Persistent Context

Context files live in `/context/`. Claude loads them on demand when you run a skill or workflow.

**Updating context (do this regularly):**
- After a major initiative milestone, update `product.md`
- After competitive intel, update `competitors.md`
- After org changes, update `team.md`
- `CLAUDE.md` gets updated when your role, priorities, or active initiatives change

Say: *"Update context/product.md to reflect that Vault v1.3 ARB is complete and we're moving to engineering sprint planning."*

---

### Running a Skill

Skills are PM frameworks you invoke by name. Claude loads the skill file, pulls relevant context, and executes.

**Examples:**
```
"Run the PRD skill for a new intelligent routing feature."
"Run the JTBD skill on the account updater experience for enterprise merchants."
"Run a competitive analysis on our hosted checkout vs. Stripe."
"Run the opportunity assessment skill on PULSE Side-by-Side Token Service."
```

**What happens:** Claude reads the skill file, loads the relevant context files, and produces a structured, decision-ready artifact — saved to `/artifacts/`.

---

### Running a Sub-Agent Review

After producing any artifact, pressure-test it before stakeholders see it.

**Examples:**
```
"Run a CTO review on this PRD."
"Run an Executive review on this roadmap."
"Run Sales and Devil's Advocate reviews on this competitive analysis."
```

**Workflow:** Produce artifact → run 2-3 agents → get structured feedback → refine → ship.

**Pro tip:** Always run Devil's Advocate on any artifact that involves a business case or revenue projection. It finds the assumption you didn't know you were making.

---

### Running a Workflow

Workflows are multi-step processes that guide you from a rough input to a reviewed artifact.

**Example session — Discovery to PRD:**
```
Step 1: "I have 3 merchant interview transcripts in /data/input/. Help me frame the problem."
Step 2: "Now run an opportunity assessment."
Step 3: "Generate 3 solution approaches."
Step 4: "Write the PRD for option 2."
Step 5: "Run CTO and Devil's Advocate reviews."
Step 6: "Update the PRD based on the feedback."
```

Full PRD, reviewed and iterated, in 60-90 minutes.

---

### Personalizing the Sub-Agents

The agents are currently pre-loaded with JPM-specific patterns. To make them even more accurate:

**Add real dialogue patterns** to each agent file:
```markdown
**[Person's name] specific patterns:**
- "They always ask about the margin impact first, before anything else."
- "Their go-to challenge is: 'what's the decommission plan for the legacy system?'"
- "They push back on timelines by asking for the engineering estimate source."
```

The more real their voice, the more useful the review.

---

## The 30-Day Plan

### Week 1: Setup & First Real Use
- [ ] Install Claude Code, set up `pm-os/` directory
- [ ] Open Claude Code, verify context loads correctly
- [ ] Run one skill on a real current initiative (Vault follow-up, IIAS defect, recon roadmap)
- [ ] Run at least one sub-agent review on an existing artifact
- [ ] Note what's missing from your context files — add it

### Week 2: Integrate Into Your Real Workflow
- [ ] Use the Discovery → PRD workflow for one new initiative
- [ ] Run all 6 agents on one PRD before sending it to engineering
- [ ] Update `context/product.md` after your first sprint planning or review
- [ ] Identify the 2-3 skills you use most — make sure they're tuned to your style

### Week 3: Customize & Extend
- [ ] Personalize agent files with real dialogue patterns from your stakeholders
- [ ] Add a new skill for something you do repeatedly (e.g., "weekly status update", "exec briefing slide")
- [ ] Set up a weekly ritual: every Monday, drop last week's research into `/data/input/`
- [ ] Run an OKR planning workflow if it's that season

### Week 4: Compound & Share
- [ ] Demo your OS to one teammate
- [ ] Export one workflow as a team-shareable SOP
- [ ] Review which context files are stale — update them
- [ ] Write a brief note to yourself: what's working, what needs tuning

---

## Weekly Maintenance Ritual (15 minutes, Monday)

```
1. Drop any new research, transcripts, or reports into /data/input/
2. Review CLAUDE.md — is the "Active Initiatives" section still current?
3. If a major initiative changed status, update context/product.md
4. Note any new competitive intel — update context/competitors.md
```

---

## Adding New Skills

When you find yourself doing the same PM activity more than twice, turn it into a skill.

**Template:**
```markdown
# Skill: [Name]

## When to Use
[One sentence]

## Inputs Required
- [Input 1]
- [Input 2]

## Instructions for Claude
[Step-by-step what Claude should do, what context files to load, what quality checks to apply]

## Output Format
Save to `/artifacts/[Name]-[topic]-[YYYY-MM-DD].md`
```

**Good candidates for new skills (based on your work):**
- "ARB Preparation Doc" — structured for Josh Moushon's architecture review board
- "Townhall Deck Slide" — single product area slide in the established format
- "Debrief / Retro" — structured initiative retrospective
- "Merchant Escalation Brief" — for executive-facing merchant issue summaries

---

## Prompting Tips for This OS

**Be specific about what you want:**
- ❌ "Help me with the Vault PRD"
- ✅ "Run the PRD skill for the Vault revelation proxy API, focusing on the SAQ-A compliance path"

**Load context explicitly when needed:**
- "Load context/competitors.md and run a competitive analysis on our debit routing vs. Stripe."

**Chain naturally:**
- "Good. Now run a CTO review on that. Then update the PRD based on the top 3 findings."

**Tell Claude when you're iterating:**
- "Version 2 — apply the executive feedback and tighten the business case section."

---

## Frequently Asked Questions

**Q: Do I need to say "load CLAUDE.md" every session?**
No. Claude Code reads it automatically when you start a session from the `pm-os/` directory.

**Q: What if Claude doesn't have enough context?**
It will ask a clarifying question. That's the right behavior — one question, then proceed.

**Q: Can I share this OS with my team?**
Yes. Give them the folder structure. They'll need to update `context/` with their own scope, team, and initiatives. The skills and agents are reusable.

**Q: How often should I update context files?**
Context files should be "alive" — update them whenever something meaningfully changes. The minimum: after every major milestone, org change, or competitive shift.

**Q: What if a skill produces something off?**
Say: "The output is too generic — apply it specifically to [context]." Or: "Redo section 3 with more focus on [specific angle]." The skill is a starting structure, not a constraint.

---

## Quick Reference Card

| Task | What to Say |
|------|------------|
| Verify context loaded | "Summarize my product scope and active priorities." |
| Run a skill | "Run the [skill name] skill on [topic]." |
| Run an agent | "Run a [agent name] review on [artifact]." |
| Run a workflow | "Start the [workflow name] workflow with [input]." |
| Update context | "Update context/[file].md to reflect [change]." |
| Save an artifact | "Save this to /artifacts/ as [filename]." |
| Add to a skill | "Add a quality check for [condition] to the PRD skill." |
