# Influx AI Design System — Foundations

## Design direction

Influx AI uses a neutral-first, Codex/ChatGPT-inspired product design language.

The visual system is intentionally restrained:

- ~90% neutral black / white / gray
- ~8% Influx Purple for primary interaction and selected states
- ~2% semantic colors for real success, warning, and error communication

Influx Purple is not a decorative color. It is a semantic emphasis color.

## Core principles

### 1. Quiet interface

The interface should recede so users can focus on content, data, and actions.

Prefer:
- typography hierarchy
- spacing
- subtle borders
- neutral surfaces
- clear component structure

Avoid:
- decorative gradients
- unnecessary shadows
- colorful cards
- multiple competing accent colors

### 2. Color has meaning

Use Influx Purple only for:
- primary actions
- active navigation
- selected state
- AI identity
- focus state
- important interactive emphasis

Use semantic colors only when they communicate state:
- green = success / active / completed
- orange = warning / needs attention
- red = error / destructive / failed
- blue = information only when necessary

Platform brand colors are allowed only inside official platform marks or logos.

Do not use Instagram pink, TikTok cyan/red, YouTube red, etc. as generic UI colors.

### 3. Hierarchy through type and space

Create hierarchy primarily through:
1. font size
2. font weight
3. spacing
4. alignment
5. border / surface contrast
6. color only when needed

### 4. One semantic pattern = one component

Influx should have one canonical design for:
- buttons
- search
- filters
- tabs
- inputs
- cards
- tables
- drawers
- modals
- tags
- status
- pagination
- empty states
- loading states

Do not reinvent a component on a page-by-page basis.

### 5. Product density matches task density

Operational interfaces should be compact and efficient.

Use more breathing room only when:
- onboarding
- AI prompt entry
- educational hero
- empty state
- complex explanation

### 6. Borders before shadows

Use borders and surface differences to establish hierarchy.

Shadows are reserved for floating layers such as:
- dropdowns
- popovers
- modals
- drawers
- floating menus

### 7. Standard patterns before custom patterns

Before introducing any new pattern, check whether an existing Influx component already solves the same semantic problem.

## Visual character

Influx should feel:
- calm
- modern
- intelligent
- precise
- professional
- lightweight
- global

Influx should not feel:
- playful consumer AI
- cyberpunk
- heavily decorative
- overly colorful
- glassmorphic
- dashboard-heavy for its own sake

## Layout philosophy

A typical page should follow:

```text
Global Sidebar
└── Top Navigation
    └── Page Content
        ├── Page Header
        ├── Optional Tabs
        ├── Search / Filter / Actions
        └── Main Content
```

For workspace pages:

```text
Sidebar
Top Navigation
└── Workspace
    ├── Control / Task Area
    └── Main Output / Preview / Content Area
```

The user task should determine the layout, not the database structure.
