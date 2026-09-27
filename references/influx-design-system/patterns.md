# Influx AI Design System — Product Patterns

## 1. Standard list page

Canonical structure:

```text
Page Header
Tabs / Context
Search
Primary Filters
More Filters
Result Count + Sort
Table / List
Pagination
```

Rules:
- search first
- filters second
- data third
- one dominant action if needed
- avoid large decorative cards on operational list pages

Use for:
- Creator Marketplace
- Campaigns
- Asset Library
- Search History
- Competitors

## 2. Detail page

Canonical structure:

```text
Identity / title
Primary actions
Summary / key metrics
Tabs
Detail content
```

Use tabs only for true peer sections.

Prefer Drawer if users must preserve list context.

Use full page if:
- editing is complex
- workflow is multi-step
- deep navigation is needed

## 3. Settings / personal center

Use:
- restrained page title
- neutral cards or sections
- left local settings navigation if needed
- high information density without dashboard decoration

Do not turn settings into a colorful analytics dashboard unless analytics is itself the user task.

## 4. Workspace

Workspace layout should prioritize the active task.

Common structure:

```text
Global Nav
Top Nav
└── Workspace
    ├── Control panel / task panel
    └── Preview / output / content area
```

Control panel should not consume excessive width.

Recommended desktop split:
- control area: ~34–42%
- output / preview: ~58–66%

For very dense controls:
- fixed or bounded control column
- flexible output region

Recent history may live inside the control area when it supports the same task.

## 5. Dashboard

Only use a dashboard when users need to compare multiple metrics or monitor state.

Avoid using dashboard layout as a default home screen.

Prefer:
- 3–5 meaningful metrics
- clear hierarchy
- neutral data visualization
- Brand Purple for the primary series or key metric only

## 6. AI Tools gallery

Structure:

```text
Page Header
Category Tabs
Tool Grid
```

Tool cards use the same visual shell.

Do not color-code every tool.

Primary differentiation should come from:
- icon
- title
- description

## 7. Outreach / Email workspace

Recommended structure:

```text
Campaign / Sequence list
Main sequence workspace
Header + status
Metrics
Sequence steps
Preview / Edit action
```

Use neutral step cards.

Use Brand Purple for:
- active step
- selected tab
- New Campaign
- primary action

Use green only for:
- positive performance
- active/completed status

## 8. Creator Marketplace

Recommended structure:

```text
Platform Tabs
Search
Primary Filters
More Filters
Result Count + Sort
Creator Table
```

Platform tabs use neutral UI.
Official platform logo may keep brand color.

Do not tint the whole tab or filter with platform brand colors.

## 9. Personal center / profile analytics

Use a calm information hierarchy.

Recommended:

```text
Profile identity
Account metadata
Key metrics
Activity visualization
Feature usage
Recent activity
```

Charts:
- Neutral 200/300 historical data
- Brand 500 primary series
- Neutral 500 secondary series

Avoid multi-color chart palettes unless multiple semantic series must be distinguished.

## 10. Responsive behavior

When width decreases:
- move secondary filters into More Filters
- reduce table columns by priority
- convert drawers to full-screen on narrow widths
- preserve primary action
- keep platform selection visible when critical
- avoid shrinking controls below usable touch/click sizes

Responsive behavior should follow priority, not just breakpoints.
