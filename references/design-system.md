# AI Product Design — Design System Router

This file is the design-system entry point for the AI Product Design skill.

For Influx AI product work, the Influx AI Design System is authoritative and must be used before creating or revising UI.

---

# Influx AI Design System

## Design direction

Influx AI follows a neutral-first, Codex/ChatGPT-inspired visual system.

Core rule:

> Default every component to black, white, and neutral gray. Use Influx Purple only for primary actions, active/selected states, AI identity, focus states, and important interactive emphasis.

Approximate visual color ratio:

```text
Neutral black / white / gray    ~90%
Influx Purple                    ~8%
Semantic status colors           ~2%
```

Influx Purple is a semantic emphasis color, not a decorative color.

Platform colors are allowed only inside official platform identity marks/logos.

Do not allow Instagram pink, TikTok cyan/red, YouTube red, or other platform colors to spread into tabs, filters, cards, backgrounds, tables, or buttons.

Semantic green/orange/red should appear only when the product genuinely communicates success, warning, error, destructive action, or status.

---

# Mandatory loading order

For Influx UI work, read these references before making design decisions:

1. `influx-design-system/foundations.md`
2. `influx-design-system/tokens.md`
3. `influx-design-system/typography.md`
4. `influx-design-system/components.md`

Then load task-specific references:

- Page structure / list / detail / workspace / outreach / profile / AI Tools:
  `influx-design-system/patterns.md`
- AI Search / AI generation / prompt / progress / retry:
  `influx-design-system/ai-patterns.md`
- Creator imagery / icons / hero graphics / chart / generated assets:
  `influx-design-system/asset-guidelines.md`

Do not design a screen first and retrofit the system afterward.

Use:

```text
Product intent
→ Product logic
→ Information architecture
→ Influx Design System
→ Existing components
→ Screen
→ States
→ Implementation
```

---

# Influx guardrails

## 1. Neutral-first components

These should normally remain neutral:

- sidebar
- top navigation
- cards
- inputs
- search
- filters
- tables
- tags
- dropdowns
- modals
- drawers
- secondary buttons
- pagination
- empty states
- loading states

Do not color-code ordinary components.

## 2. Brand Purple usage

Use Influx Purple for:

- Primary CTA
- Active / selected navigation
- Selected tab or state when emphasis is needed
- AI identity
- Focus ring
- Key link
- Important interactive emphasis

Do not use Purple simply to make the page feel branded.

## 3. Existing component first

Before introducing any new UI pattern, check whether an existing Influx component already solves the same semantic problem.

One semantic pattern = one canonical component.

Influx should not have different versions of:
- Search
- Filter
- Select
- Tabs
- Button
- Table
- Card
- Drawer
- Modal
- Tag
- Pagination

unless behavior genuinely differs.

## 4. Hierarchy before decoration

Use:
- font size
- font weight
- spacing
- alignment
- border
- neutral surface contrast

before introducing more color, shadow, or decoration.

## 5. Borders before shadows

Operational components should normally use a subtle neutral border and no shadow.

Use shadow only for real elevation:
- dropdown
- popover
- modal
- floating layer

## 6. Asset discipline

Product imagery must follow `asset-guidelines.md`.

Prefer:
1. real UI/product visualization
2. creator photography
3. data visualization
4. simple line icons
5. illustration

Avoid decorative AI imagery unless it clarifies the product.

---

# Core visual defaults

## Typography

Preferred:
```text
Inter / SF Pro / system-ui
```

Weights:
```text
400 / 500 / 600
```

Primary UI sizes:
```text
Display        32 / 40 / 600
Page Title     24 / 32 / 600
Section Title  18 / 26 / 600
Card Title     16 / 24 / 600
Body           14 / 22 / 400
Body Strong    14 / 22 / 500
Secondary      13 / 20 / 400
Caption        12 / 18 / 400
Micro          11 / 16 / 500
```

## Spacing

Use a 4px grid:

```text
4 / 8 / 12 / 16 / 20 / 24 / 32 / 40 / 48 / 64
```

## Radius

```text
6 / 8 / 10 / 12 / 16
```

Operational controls should generally use 8px.

Cards generally use 12px.

Large hero/modal surfaces may use 16px.

## Standard control height

```text
Input / Select / Filter / Button: 40px
Large Search: 44–48px
```

---

# Required quality check

Before finalizing any Influx UI, verify:

### Brand discipline
- Is most UI neutral?
- Is Purple used only for meaningful emphasis?
- Are platform colors isolated to platform marks?
- Are semantic colors tied to real semantics?

### Component consistency
- Does search match Influx Search?
- Do filters match canonical filters?
- Are selected states consistent?
- Are button levels correct?
- Is table behavior consistent?
- Are cards neutral?

### Typography
- Are semantic type roles used?
- Are there too many font sizes?
- Are weights limited to 400/500/600?

### Spacing
- Does spacing follow the 4px system?
- Are major regions separated more than related controls?

### Product hierarchy
- Is one main action obvious?
- Is the page optimized for the user task?
- Is visual decoration secondary to content?

### Assets
- Do images follow the correct ratio?
- Are creator images realistic and consistent?
- Are icons from one icon family?
- Are charts neutral-first?

If these checks fail, fix the design system usage before polishing the page.

---

# Reference library

- [Foundations](./influx-design-system/foundations.md)
- [Tokens](./influx-design-system/tokens.md)
- [Typography](./influx-design-system/typography.md)
- [Components](./influx-design-system/components.md)
- [Product Patterns](./influx-design-system/patterns.md)
- [AI Patterns](./influx-design-system/ai-patterns.md)
- [Asset Guidelines](./influx-design-system/asset-guidelines.md)
