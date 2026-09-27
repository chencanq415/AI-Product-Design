# AI Product Design

AI Product Design is a reusable product-design skill for turning vague product ideas into complete, coherent, implementation-ready product solutions.

It is designed for product managers, designers, founders, and AI coding workflows where the user can describe intent in incomplete natural language and let the skill fill in standard product and UI details.

## What it does

AI Product Design helps with:

- Clarifying vague requirements
- Turning intent into product logic
- Defining information architecture
- Establishing a consistent design foundation
- Reusing standard SaaS interaction patterns
- Designing pages, workflows, and states
- Filling in routine UI details without repeatedly asking the user
- Producing implementation-ready specifications for AI coding agents
- Generating full PRDs when needed

## Core philosophy

The user should describe the product intent.

The skill should own the product-design details.

That means users should not need to manually define routine patterns such as:

- how search works
- how filters are structured
- how forms validate
- how tables behave
- where loading and empty states appear
- whether a drawer or modal is appropriate
- how button hierarchy works

The skill uses mature product conventions unless a business or technical constraint requires something different.

## Design workflow

AI Product Design follows this sequence:

```text
Intent
  ↓
Product Logic
  ↓
Information Architecture
  ↓
Design System
  ↓
Component System
  ↓
Screen Design
  ↓
States & Edge Cases
  ↓
Acceptance Criteria
  ↓
Implementation Specification
```

This prevents a common AI-product-design failure mode: designing isolated screens before defining the system that connects them.

## Repository structure

```text
AI-Product-Design/
├── SKILL.md
├── README.md
└── references/
    └── design-system.md
```

### SKILL.md

The main skill instructions.

It defines:

- clarification policy
- decision hierarchy
- product-design workflow
- standard UI patterns
- redesign rules
- AI product rules
- output modes
- acceptance criteria
- implementation prompt structure

### references/design-system.md

A reusable baseline design system for SaaS and AI products.

It covers:

- layout
- spacing
- typography
- color roles
- radius and elevation
- buttons
- forms
- search
- filters
- tabs
- tables
- cards
- modals
- drawers
- feedback
- loading
- empty states
- errors
- responsive behavior
- interaction consistency

The skill should prefer an existing product's design system when one exists. This reference acts as the default when no stronger system is available.

## Example usage

### Example 1 — vague requirement

```text
I need an AI Search workspace.

Users should be able to start a new conversation, configure some parameters,
and see their conversation history.

The sidebar and top navigation should stay unchanged.
```

The skill should automatically determine:

- page hierarchy
- primary action
- composer structure
- parameter placement
- history layout
- loading states
- empty states
- error behavior
- component reuse
- implementation rules

It should only ask follow-up questions if a missing answer materially changes business or technical logic.

### Example 2 — redesign

```text
This creator list page feels messy.

We support Instagram, TikTok, and YouTube, but the backend only supports
single-platform filtering.

Please redesign the content area but keep the global navigation unchanged.
```

The skill should diagnose the structural issue first, then define:

- platform-selection behavior
- search/filter hierarchy
- table/list structure
- information architecture
- reusable components
- state behavior
- final implementation prompt

## Output modes

### Quick Design

Best for small UI adjustments.

Outputs:

1. Problem Diagnosis
2. Recommended Solution
3. Key Interaction Changes
4. Implementation Instructions

### Product Design

Default mode.

Outputs:

1. Product Intent
2. Confirmed / Assumptions / Open Questions
3. User Flow
4. Information Architecture
5. Design Foundation
6. Component Strategy
7. Screen Design
8. States & Edge Cases
9. Acceptance Criteria
10. AI Implementation Prompt

### Full PRD

Best for larger features or when a formal PRD is needed.

Includes:

- background
- goals
- non-goals
- users
- scenarios
- requirements
- user flow
- information architecture
- functional specification
- interaction specification
- design system
- states
- edge cases
- data requirements
- technical constraints
- acceptance criteria
- implementation prompt

## Recommended usage with AI coding agents

This skill is especially useful before handing work to tools such as:

- Codex
- Claude Code
- Cursor
- Trae
- other coding agents

A good workflow is:

```text
Vague requirement
→ AI Product Design
→ Product Design / PRD
→ Implementation Specification
→ Coding Agent
```

The implementation specification should be explicit about:

- what to preserve
- what to modify
- page hierarchy
- reusable components
- behavior
- states
- constraints
- acceptance criteria

## Key rule

Do not start from pixels.

Start from product intent and product logic, then build a consistent UI system around it.
