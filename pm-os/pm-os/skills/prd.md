# Skill: PRD (Product Requirements Document)

## When to Use
Creating a new PRD or structured requirements document for any feature, initiative, or platform capability.

## Inputs Required
- Feature / initiative name
- Problem statement or opportunity (can be rough)
- Any constraints or known context (optional)

## Instructions for Claude

Load `context/product.md` and `context/company.md` before executing.

Produce a structured PRD with the following sections:

---

### 1. Executive Summary
One paragraph. What, why, and what success looks like.

### 2. Problem Statement
- What problem are we solving?
- Who experiences it? (reference personas if relevant)
- What's the current state / workaround?
- What's the cost of NOT solving it?

### 3. Goals & Success Metrics
| Goal | Metric | Target | Timeframe |
|------|--------|--------|-----------|
| ... | ... | ... | ... |

### 4. Non-Goals (Explicit Out of Scope)
Bulleted list. Be specific — this prevents scope creep.

### 5. User Stories / Jobs to Be Done
Format: *"When [situation], I want to [motivation], so I can [outcome]."*
Prioritize: P0 (must-have) / P1 (should-have) / P2 (nice-to-have)

### 6. Functional Requirements
Numbered list. Each requirement:
- Priority (P0/P1/P2)
- Requirement statement (testable)
- Acceptance criteria (Gherkin format for P0s: Given/When/Then)

### 7. Non-Functional Requirements
- Performance targets
- Security / PCI requirements
- Availability / SLA
- Compliance constraints (PSD2, IIAS, network rules as applicable)

### 8. API Design (if applicable)
- Key endpoints (OpenAPI 3.0 format stubs)
- Request/response examples
- Error states

### 9. Open Questions
Numbered list of unresolved decisions with owner and due date fields.

### 10. Dependencies & Risks
| Item | Type | Impact | Mitigation |
|------|------|--------|------------|
| ... | Dependency/Risk | H/M/L | ... |

---

## Output Format
Save to `/artifacts/PRD-[initiative-name]-[YYYY-MM-DD].md`

## Quality Bar
- Every P0 requirement must have a Gherkin acceptance criterion
- Non-goals must be explicit — at least 3
- Success metrics must be measurable (no "improve user satisfaction" without a number)
