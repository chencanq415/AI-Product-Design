# AI Product Design — Default Design System Reference

This document provides the default SaaS and AI-product design foundation for the AI Product Design skill.

Use it when the target product does not already have a stronger existing design system.

If an existing codebase or product already defines a component library or interaction pattern, prefer the existing system and use this file only to fill gaps.

---

# 1. Design Principles

## 1.1 Consistency over novelty

Use one semantic component for one semantic purpose.

The same action should look and behave the same across the product.

## 1.2 Hierarchy before decoration

Users should understand:

- where they are
- what matters
- what they can do
- what happens next

before any decorative styling is added.

## 1.3 Standard patterns by default

Prefer mature conventions for:

- search
- filters
- forms
- tables
- navigation
- dialogs
- feedback

Create custom interactions only when standard patterns fail the product requirement.

## 1.4 Reduce cognitive load

Expose common actions first.

Hide advanced controls until needed.

Avoid presenting every setting, filter, and action at equal visual priority.

## 1.5 Product density should match task density

Data-heavy operational products can be compact.

Creative or exploratory products can be more spacious.

Do not use large marketing-style cards inside dense workspaces unless they have a clear purpose.

---

# 2. Layout

## 2.1 Page structure

Typical application page:

```text
Global Navigation
└── Page Container
    ├── Page Header
    │   ├── Title / Context
    │   ├── Secondary Actions
    │   └── Primary Action
    ├── Optional Tabs / Sub-navigation
    ├── Search & Filters
    └── Main Content
```

## 2.2 Content width

For application workspaces:

- allow fluid width where tables or complex workflows need it
- constrain reading-heavy content
- avoid excessive empty margins in dense SaaS products

## 2.3 Grid

Prefer simple layouts:

- 1-column for primary workflows
- 2-column for content + contextual panel
- 3-column only when each region has a persistent responsibility

Do not create dashboard grids simply to fill space.

---

# 3. Spacing

Use a consistent spacing scale.

Recommended baseline:

```text
4
8
12
16
24
32
40
48
64
```

Typical usage:

- 4–8: icon/text, tightly related controls
- 12–16: field and component internal spacing
- 16–24: related component groups
- 24–32: sections
- 40–64: major page regions

Avoid arbitrary one-off spacing values.

---

# 4. Typography

Define semantic roles rather than styling text independently on every page.

Recommended roles:

## Page Title

Primary page heading.

Use sparingly: normally one per page.

## Section Title

Separates major content regions.

## Card / Panel Title

Used for contained subsections.

## Body

Default readable content.

## Label

Form labels, column labels, metadata labels.

## Secondary Text

Supporting information.

## Caption

Low-priority metadata such as timestamps or helper text.

Use font weight and size together to create hierarchy.

Do not rely on color alone.

---

# 5. Color Roles

Use semantic roles instead of hard-coded page-specific colors.

Required roles:

- Background
- Surface
- Surface Elevated
- Border
- Text Primary
- Text Secondary
- Text Disabled
- Primary
- Primary Hover
- Success
- Warning
- Error
- Info
- Disabled

Use brand color mainly for:

- primary actions
- active navigation
- selected states
- meaningful emphasis

Do not flood the interface with brand color.

---

# 6. Radius

Use a small, repeatable radius scale.

Recommended:

- Small: inputs, tags, compact controls
- Medium: buttons, cards, panels
- Large: major containers only when the product style calls for it

Avoid mixing unrelated rounded styles across pages.

---

# 7. Elevation

Prefer borders and surface contrast before shadows.

Use elevation only when semantic layering exists:

- dropdown
- popover
- modal
- floating action
- draggable or overlapping surface

Avoid shadows on every card.

---

# 8. Iconography

Use one icon family.

Rules:

- match stroke/fill style across the product
- do not mix multiple icon families casually
- use icons to reinforce actions, not replace unclear labels
- include tooltips for ambiguous icon-only actions

---

# 9. Buttons

Use a clear action hierarchy.

## Primary Button

Use for the most important action in the current context.

Normally one dominant primary action per region.

## Secondary Button

Use for important alternatives.

## Tertiary / Text Button

Use for low-emphasis actions.

## Destructive Button

Use only for destructive actions.

Never style a destructive action as a normal primary action.

## Icon Button

Use when the action is common and recognizable.

Add tooltip where meaning may be unclear.

### Button behavior

Support:

- default
- hover
- active
- focus
- disabled
- loading

Loading buttons should preserve width to prevent layout shift.

---

# 10. Forms

## 10.1 Field structure

Use:

```text
Label
Input
Helper / Validation
```

Labels should remain visible.

Do not rely on placeholder text as the only label.

## 10.2 Required vs optional

Choose one convention and apply it consistently.

A common pattern:

- mark optional fields as “Optional”
- assume unmarked fields are required when most fields are required

## 10.3 Validation

Validation should:

- appear close to the affected field
- explain how to resolve the problem
- preserve entered data
- run at an appropriate moment

Avoid showing errors before the user has interacted unless the action has been submitted.

## 10.4 Long forms

Split long forms by meaningful sections.

Use multi-step flows only when steps have meaningful progression.

Do not create wizard steps merely to make the form look simpler.

---

# 11. Search

A standard search component should include:

- search icon
- meaningful placeholder
- clear action when content exists
- keyboard submit where relevant
- loading feedback for remote queries
- empty-result behavior
- persistence with active filters

## Real-time search

Use debounce for remote search where appropriate.

Do not fire a network request on every keystroke without reason.

## Search scope

Make scope explicit when users may misunderstand what is being searched.

---

# 12. Filters

Default pattern:

```text
Search
Primary Filters
More Filters
Clear All
```

## Primary filters

Expose commonly used filters.

## Secondary filters

Put less frequent filters in:

- More Filters popover
- drawer
- advanced filter panel

## Active filters

Show:

- selected values
- active filter count
- clear individual filter
- Clear All

Do not force users to remember hidden active filters.

## Filter application

Choose one behavior:

### Immediate apply

Good for fast, local, low-cost filtering.

### Apply button

Better for:

- expensive queries
- multiple dependent filters
- complex advanced filtering

Use one model consistently within the same product.

---

# 13. Tabs

Use tabs when sections:

- are peers
- share the same context
- are frequently switched
- do not represent fundamentally different navigation destinations

Avoid tabs when:

- they hide unrelated workflows
- they create too many levels of navigation
- they exist only because content was difficult to organize

Support clear:

- default
- hover
- active
- disabled states

---

# 14. Tables

Use tables for structured, comparable data.

A standard table may include:

- primary identifier
- key attributes
- status
- owner
- updated time
- actions

## Column priority

Put the most important identification information first.

Keep low-value metadata later.

## Sorting

Only add sorting where users benefit from it.

Show active sort direction clearly.

## Row actions

Prefer:

- direct actions for common tasks
- overflow menu for secondary actions

## Selection

Add checkboxes only when bulk actions exist.

Do not add selection without a purpose.

## Pagination

Use pagination for large bounded datasets.

Consider infinite loading only when browsing is more important than precise navigation.

## Horizontal scrolling

Avoid if possible.

When unavoidable:

- keep key identifier columns visible if supported
- prioritize columns carefully

---

# 15. Lists

Use lists when content has more flexible structure than a table.

Each item should make the primary identity and key action easy to scan.

Avoid turning every list item into an oversized card.

---

# 16. Cards

Use cards when content benefits from clear grouping.

Cards should not become the default container for every piece of content.

Avoid:

- card-inside-card nesting
- excessive shadows
- large padding in dense operational products

---

# 17. Modal

Use modal for:

- confirmation
- short input
- focused decisions
- small edits

Avoid modal for:

- complex creation workflows
- multi-section editing
- tasks needing comparison with background content

Support:

- escape / close behavior when safe
- clear primary and secondary actions
- destructive confirmation where needed

---

# 18. Drawer

Use drawer for contextual detail when retaining the underlying page matters.

Good use cases:

- record details
- lightweight edit
- preview
- configuration
- contextual inspection

Use a full page instead when the task becomes complex or requires deep navigation.

---

# 19. Dropdown and Popover

Use for compact, contextual actions or choices.

Close on:

- explicit selection where appropriate
- outside click
- escape

Do not put large workflows into dropdowns.

---

# 20. Feedback

## Toast

Use for transient confirmation.

Examples:

- saved
- copied
- invite sent

Do not use toast as the only place for critical errors.

## Alert

Use for persistent or important information.

## Inline feedback

Use close to the object or field when action is local.

---

# 21. Loading States

Choose the loading pattern that matches the operation.

## Skeleton

Best when page structure is known.

## Spinner

Best for compact operations.

## Progress indicator

Best for multi-step or long-running operations.

Do not leave a blank interface during loading.

For AI operations, show meaningful progress when available.

---

# 22. Empty States

Differentiate:

## First-use empty state

Explain:

- what this area is
- why it is empty
- the primary next action

## No search results

Explain that no results match the query.

Offer:

- clear search
- clear filters
- broaden criteria

## No permission / unavailable data

Do not present this as a normal empty dataset.

Explain the actual state.

---

# 23. Error States

Errors should answer:

1. What happened?
2. What can the user do?
3. Is their work preserved?

Prefer actionable language.

Avoid generic messages such as:

“Something went wrong”

when more useful information is available.

For recoverable errors, provide Retry.

---

# 24. Destructive Actions

Use confirmation when the action:

- cannot be easily undone
- causes meaningful data loss
- affects other users
- changes billing or permissions

Confirmation should name the object and consequence.

For lower-risk actions, prefer undo over confirmation when feasible.

---

# 25. Navigation

Navigation should reflect product structure, not implementation architecture.

## Sidebar

Use for stable top-level product areas.

Do not overload the sidebar with every possible sub-feature.

## Top navigation

Use for global context, workspace controls, account, and cross-product actions.

## Breadcrumb

Use when hierarchy is deep enough that users benefit from location context.

Do not add breadcrumbs to shallow products.

---

# 26. Status

Use clear semantic states.

Examples:

- Draft
- Active
- Paused
- Completed
- Failed

Do not encode status using color alone.

Use text plus visual treatment.

---

# 27. Tags and Badges

Use tags for:

- categories
- attributes
- filters
- compact metadata

Use badges for:

- status
- count
- small semantic indicators

Avoid excessive colored pills.

---

# 28. AI Product Patterns

AI interfaces should distinguish:

## User Input

What the user explicitly controls.

## System Configuration

Model, parameters, constraints, data scope.

## AI Output

Generated content or results.

## System State

Thinking, searching, generating, failed, partial, complete.

### AI operations should consider:

- streaming
- stop
- retry
- regenerate
- edit and rerun
- version history
- source references
- partial completion
- failure recovery
- persistent context
- user control

Do not hide meaningful AI uncertainty behind deterministic-looking UI.

---

# 29. Responsive Behavior

Desktop SaaS products should still degrade gracefully.

When width becomes limited:

- collapse secondary controls
- move secondary filters into More Filters
- prioritize critical table columns
- allow drawers to become full-screen where appropriate
- avoid preserving desktop density at the expense of usability

Define responsive behavior by priority, not just by breakpoint.

---

# 30. Interaction Consistency Checklist

Before finalizing any screen, verify:

- Does search behave like search elsewhere?
- Do filters follow the same pattern?
- Are primary actions styled consistently?
- Are forms using the same label and validation rules?
- Are tables using the same row/action conventions?
- Are modal and drawer decisions consistent?
- Are loading and empty states consistent?
- Are errors recoverable?
- Are selected and active states obvious?
- Are repeated components truly reusable?

If not, fix the system before polishing the screen.
