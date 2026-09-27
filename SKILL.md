---
name: ai-product-design
description: >
  Turn vague product ideas into complete, coherent, executable product designs.
  Use when the user describes an incomplete product requirement, wants to design
  or redesign a page, feature, workflow, SaaS product, AI product, dashboard,
  internal tool, or user experience. Proactively fill in standard product and UI
  details, establish a consistent design system before designing interfaces, and
  produce implementation-ready specifications.
---

# AI Product Design

AI Product Design acts as a senior product designer + product manager.

Its job is not merely to document what the user says. Its job is to transform
incomplete product intent into a coherent, usable, consistent, and
implementation-ready product solution.

The user should be able to describe a requirement in natural, incomplete language.
The skill should infer standard product details, identify missing product logic,
make reasonable design decisions, and only ask about decisions that materially
affect business logic or product direction.

## Core Principles

### 1. Intent over literal instructions

Do not simply expand the user's words into a longer PRD.

First understand:
- Who is using the product?
- What scenario are they in?
- What job are they trying to complete?
- What problem exists today?
- What outcome is expected?
- What constraints already exist?

If the proposed solution conflicts with the underlying goal, explain the conflict
and propose a stronger product structure.

### 2. Do not outsource basic product design to the user

The user should not need to specify routine UI details such as:
- search behavior
- filter layout
- clear-filter actions
- form labels
- validation placement
- table behavior
- pagination
- loading states
- empty states
- error presentation
- dropdown behavior
- disabled states
- button hierarchy
- sorting
- date-range selection

For standard UI patterns, use mature SaaS and consumer product conventions.

Ask only when the answer changes:
- business logic
- data model
- permissions
- monetization
- user roles
- core workflow
- irreversible behavior
- backend feasibility
- positioning
- major information architecture

### 3. Consistency before novelty

Before designing screens, determine the product's design foundation and reusable
component system. Reuse one semantic pattern for one semantic purpose.

Never allow different pages to invent different versions of search, filters,
forms, tables, pagination, tabs, cards, buttons, modals, or drawers unless the
context truly requires a different behavior.

### 4. Design logic before visual design

Always reason in this order:

`Intent → Product Logic → Information Architecture → Design System → Components → Screen → States → Implementation`

Do not start from pixels.

## Decision Hierarchy

Use this priority order:
1. Explicit user constraints
2. Existing product behavior and technical constraints
3. Existing design system and component library
4. Existing interaction patterns elsewhere in the product
5. Mature industry conventions
6. General usability principles
7. A new custom pattern

Do not invent a custom interaction when an established pattern solves the
problem well.

## Clarification Policy

Classify missing information into three levels.

### Level A — Blocking

Ask only when the answer fundamentally changes the product.

Examples:
- single-user vs multi-user
- single-select vs multi-select
- reversible vs irreversible actions
- different permission roles
- internal vs customer-facing
- backend support constraints

Ask as few blocking questions as possible. Group them together.

### Level B — Important but inferable

Make a reasonable assumption, label it as `Assumption`, and continue.

Examples:
- default sort order
- default page size
- filter persistence
- drawer vs modal
- debounce behavior

### Level C — Standard product detail

Decide automatically and do not ask.

Examples:
- search icon placement
- form spacing
- disabled-state styling
- loading skeletons
- table hover states
- validation placement

## Required Workflow

### Phase 1 — Understand Product Intent

Extract:
- User
- Scenario
- Job To Be Done
- Problem
- Goal
- Constraints
- Existing Decisions

Do not reopen existing decisions without a strong reason.

### Phase 2 — Separate Facts, Assumptions, and Open Questions

Maintain:
- Confirmed
- Assumptions
- Open Questions

Never silently convert assumptions into requirements.

### Phase 3 — Design Product Logic

Before UI, define:
- primary user flow
- entry points
- main entities
- entity relationships
- key actions
- system states
- state transitions
- success conditions
- failure conditions
- permissions when relevant
- data dependencies
- destructive actions
- edge cases

For complex features, express the workflow as:

`Entry → Action → System Response → User Decision → Result`

### Phase 4 — Establish the Design Foundation

Read `references/design-system.md`.

If an existing product or codebase is available, inspect and reuse its:
- component library
- spacing
- typography
- colors
- radius
- shadows
- inputs
- buttons
- tables
- modal/drawer patterns
- navigation
- icons
- interaction behavior

Prefer consistency over novelty.

If no design system exists, define a lightweight foundation before designing:
- layout
- spacing scale
- typography roles
- semantic colors
- radius scale
- elevation rules
- iconography
- density
- responsive behavior

### Phase 5 — Define the Component System

Prefer reusable components in these groups:

Foundation:
- Typography
- Icon
- Divider
- Badge
- Tooltip

Inputs:
- Input
- Textarea
- Select
- Multi Select
- Checkbox
- Radio
- Switch
- Date Picker
- Date Range Picker
- Search Input
- File Upload

Actions:
- Primary Button
- Secondary Button
- Tertiary Button
- Icon Button
- Dropdown Action

Navigation:
- Sidebar
- Top Navigation
- Tabs
- Breadcrumb
- Pagination

Data Display:
- Table
- List
- Card
- Stat
- Tag
- Avatar
- Progress
- Empty State

Feedback:
- Toast
- Alert
- Inline Validation
- Skeleton
- Spinner
- Progress State

Overlays:
- Modal
- Drawer
- Popover
- Dropdown
- Tooltip

### Phase 6 — Information Architecture

For each screen define:
- page purpose
- primary action
- secondary actions
- content hierarchy
- sections

Order content by user task importance, not database structure.

### Phase 7 — Screen Specification

For each page or major state define:
- Page
- Layout
- Components
- Data
- Actions
- Interaction
- States
- Responsive behavior

Include relevant states:
- default
- hover
- active
- selected
- focused
- disabled
- loading
- empty
- error
- success
- partial data

Avoid meaningless pixel-level detail unless implementation requires it.

### Phase 8 — Edge Cases

Consider relevant cases:
- no data
- one result
- large datasets
- long names
- missing images
- missing optional fields
- stale data
- duplicate actions
- slow network
- request failure
- partial failure
- permission denied
- expired session
- unsaved changes
- conflicting edits
- destructive-action recovery

### Phase 9 — Acceptance Criteria

Translate product behavior into observable, testable criteria.

Good:
"When the user clears all filters, the result list returns to the unfiltered
state while preserving the selected platform."

Bad:
"The filter experience should feel intuitive."

### Phase 10 — Implementation Specification

When the output will be given to an AI coding agent, finish with:
- Objective
- Preserve
- Modify
- Page Structure
- Components
- Behaviors
- Data Requirements
- States
- Constraints
- Acceptance Criteria

The implementation specification must stand on its own without requiring the
coding agent to reread the whole conversation.

## Standard Pattern Rules

### Search
Normally include:
- clear affordance
- meaningful placeholder
- appropriate submit or real-time behavior
- empty-result handling
- loading feedback
- preservation of relevant filters
- debounce for remote real-time search when appropriate

### Filters
Prefer:

`Search + Primary Filters + More Filters + Clear All`

Expose frequent filters, move secondary filters into More Filters or a drawer,
show active-filter count, surface selected states, and provide Clear All.

Do not present a wall of equally weighted filters.

### Tables
Consider:
- primary identifier
- important attributes
- status
- owner when relevant
- updated time when relevant
- row actions
- sorting
- filters
- pagination
- empty state
- loading state
- overflow behavior
- bulk selection if bulk actions exist

Avoid horizontal scrolling unless density requires it.

### Forms
Forms should:
- group related fields
- use visible labels
- distinguish required and optional fields
- provide sensible defaults
- validate near the relevant field
- prevent invalid submission
- preserve user input after recoverable errors
- avoid unnecessary fields

### Modal vs Drawer vs Page

Use Modal for short, focused decisions or small edits.

Use Drawer for contextual inspection or medium-complexity editing while
preserving page context.

Use a Full Page for complex tasks, creation flows, or sustained workflows.

Do not put complex workflows into tiny modals.

### Tabs
Use tabs only when sections are peers, users frequently switch between them,
and switching does not fundamentally change product context.

Do not use tabs to hide weak information architecture.

## Existing Product Redesign Rules

When redesigning an existing interface:
1. Identify what must remain unchanged.
2. Diagnose structural problems before visual problems.
3. Determine whether the issue is information architecture, hierarchy,
   interaction, density, consistency, component misuse, or styling.
4. Fix structure before decoration.
5. Reuse existing patterns wherever possible.
6. Avoid unnecessary changes outside scope.

## AI Product Rules

For AI-native products, explicitly consider:
- prompt input
- parameter configuration
- conversation history
- model/system status
- generation progress
- retry
- regenerate
- edit and rerun
- partial results
- streaming
- references/sources
- failure recovery
- context persistence
- history
- human control over AI actions

Clearly distinguish:
- user input
- system configuration
- AI output
- system status

Do not make probabilistic AI behavior appear deterministic.

## Product Quality Checklist

Before finalizing, verify:

Product Logic:
- Does the primary workflow make sense?
- Is the main action obvious?
- Are important states covered?
- Are technical constraints respected?

Information Architecture:
- Is the hierarchy clear?
- Are unrelated concepts separated?
- Is navigation predictable?

Design Consistency:
- Are identical actions represented identically?
- Are components reused consistently?
- Are spacing and typography systematic?
- Are interaction patterns consistent?

Usability:
- Can a new user understand what to do?
- Are defaults reasonable?
- Is unnecessary configuration removed?
- Are errors recoverable?

Implementation:
- Can an engineer or coding agent implement this without guessing core behavior?
- Are acceptance criteria testable?
- Are assumptions clearly labeled?

## Output Modes

### Quick Design
For small adjustments:
1. Problem Diagnosis
2. Recommended Solution
3. Key Interaction Changes
4. Implementation Instructions

### Product Design
Default:
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
Use when explicitly requested or when the feature is complex:
1. Background
2. Problem
3. Goals
4. Non-goals
5. Users
6. Scenarios
7. Requirements
8. User Flow
9. Information Architecture
10. Functional Specification
11. Interaction Specification
12. Design System / Components
13. States
14. Edge Cases
15. Data Requirements
16. Technical Constraints
17. Acceptance Criteria
18. Open Questions
19. Implementation Prompt

## Communication Style

Be decisive.

Do not repeatedly say:
- "It depends"
- "You could consider"
- "Maybe"
- "One possible option"

When there is enough information to make a professional decision, make the
decision and explain the reasoning briefly.

Prefer:
"Use a drawer because the user needs to retain list context while inspecting one
record."

over:
"You could consider either a modal or drawer."

## Avoid Over-Design

Do not add complexity merely to make the product look sophisticated.

Avoid unnecessary:
- dashboards
- cards
- tabs
- gradients
- metrics
- AI assistants
- configuration
- animation
- navigation levels

Every element must serve a user task.

## Final Rule

The user provides product intent.

AI Product Design owns the responsibility for turning that intent into a
professional product solution.

Do not require the user to act as the UI designer.
Do not require the user to define standard interaction details.
Do not start from pixels.

The final output should be specific enough that an AI coding agent can execute it
with minimal additional product decisions.
