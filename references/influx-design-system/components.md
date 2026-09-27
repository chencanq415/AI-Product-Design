# Influx AI Design System — Components

## 1. Buttons

### Primary Button

Use for the most important action in the current context.

```text
Height: 40px
Horizontal padding: 16px
Radius: 8px
Font: 14 / 500
Background: Brand 600
Text: White
```

Hover:
- Brand 700

Disabled:
- Neutral 100 background
- Neutral 400 text

Examples:
- Search with AI
- Generate
- Create Campaign
- Save
- Confirm

Rule: normally one dominant primary action per visual region.

### Secondary Button

```text
Height: 40px
Background: White
Border: Neutral 200
Text: Neutral 900
```

Examples:
- View
- Edit
- More Filters

### Tertiary Button

Transparent, no border.

Examples:
- View all
- Clear all
- Cancel

### Destructive Button

Use only for genuinely destructive actions.

Do not reuse Primary Purple for destructive actions.

### Icon Button

```text
32 × 32px
Radius: 8px
```

Use for:
- favorite
- more
- close
- edit

Add tooltip when meaning is not universally obvious.

---

## 2. Selection

Selected states should be subtle.

```text
Background: Brand 50
Border: Brand 300
Text/Icon: Brand 600
```

Do not fill large selected surfaces with saturated purple.

---

## 3. Sidebar navigation

Recommended width:
```text
220–240px
```

Nav item:
```text
Height: 40px
Radius: 8px
Horizontal padding: 12px
Gap: 10px
```

Default:
- icon Neutral 500
- text Neutral 600

Hover:
- background Neutral 50
- text Neutral 900

Selected:
- background Brand 50
- icon Brand 600
- text Brand 600

---

## 4. Top navigation

```text
Height: 64px
Background: White
Bottom border: Neutral 200
```

Avoid heavy shadow.

---

## 5. Tabs

Default:
- text Neutral 500

Active:
- text Neutral 900
- 2px bottom border Brand 500

Use for peer sections.

Avoid large colored pill tabs unless the control is actually a segmented filter.

---

## 6. Input

Standard:
```text
Height: 40px
Radius: 8px
Background: White
Border: Neutral 200
Text: 14px
Placeholder: Neutral 400
```

Focus:
- border Brand 400
- 2px Brand 100 focus ring

Large search:
- 44–48px height

---

## 7. AI Prompt Composer

Use for natural-language AI requests.

```text
Min-height: 120–140px
Padding: 16px
Radius: 12px
Border: Neutral 200
Background: White
```

Optional bottom action row:
- Attach
- Mode
- References
- Context source

Primary AI action should remain visually distinct.

Do not style every text area like an AI composer.

---

## 8. Search

Standard structure:

```text
[Search icon] Placeholder                         [Clear]
```

Height: 40px.

Use standard search for:
- creator marketplace
- campaign list
- history
- asset library

Use AI Prompt Composer for:
- AI Search
- AI generation
- natural-language exploration

---

## 9. Filters

Canonical structure:

```text
Search
Primary Filters
More Filters
Clear All
```

Standard filter:
```text
Height: 40px
Background: White
Border: Neutral 200
Radius: 8px
Value + Chevron
```

Selected:
- Brand 300 border
- Brand 600 value

Do not color filters by category or platform.

---

## 10. Filter Chips

```text
Height: 24–28px
Background: Neutral 100
Text: Neutral 600
Radius: 6px or pill
```

Examples:
- US
- Beauty
- 10K–500K
- >3%

Do not use colorful chips by default.

---

## 11. Tags

Standard tag:
- Neutral 100 background
- Neutral 600 text

Use for:
- Beauty
- Lifestyle
- Travel
- Wellness

Platform identity color may appear only in official logo/mark.

---

## 12. Status

Use semantic colors only for real states.

Examples:
- Active → green
- Completed → green
- Draft → gray
- Paused → gray/orange
- Failed → red

Use soft backgrounds:
- semantic 50-level background
- darker semantic text

Never rely on color alone: always include a status label.

---

## 13. Table

Header:
```text
Height: 40px
Background: Neutral 50
Text: 11–12px / Neutral 500
```

Row:
```text
Min-height: 64px
Bottom border: Neutral 200
```

Hover:
- Neutral 25 / Neutral 50

Do not use zebra striping.

Row content hierarchy:

```text
Primary: Yoya Anna
Secondary: @yoga_anna
Metadata: Wellness · Fitness
```

Checkboxes appear only if bulk actions exist.

---

## 14. Card

Default:
```text
Background: White
Border: Neutral 200
Radius: 12px
Shadow: none
```

Hover:
- border Neutral 300

Do not assign a different color to each card.

---

## 15. AI Tool Card

Structure:

```text
Icon container
Title
Description
Action
```

Icon container:
- 32×32
- Neutral 100
- Neutral 900 icon

Only a core AI capability may use Brand 50 / Brand 600.

Do not color each AI tool differently.

---

## 16. Modal

Common widths:
- 480
- 560
- 640

```text
Radius: 16
Background: White
```

Structure:
- Title
- Description
- Content
- Footer actions

---

## 17. Drawer

Typical width:
- 480–640px

Use for:
- Creator Detail
- Campaign Detail
- Email Preview
- Contextual Editing

Use full page when the task becomes complex.

---

## 18. Dropdown / Popover

```text
Background: White
Border: Neutral 200
Radius: 10
Shadow: subtle
Padding: 6
```

Item:
- height 36
- radius 6

Hover:
- Neutral 100

Selected:
- Brand 50
- Brand 600

---

## 19. Pagination

Use neutral controls.

Current page:
- Brand 50 or Brand 600 depending density
- prefer subtle emphasis over a large saturated block

Disabled:
- Neutral 300 / 400

---

## 20. Feedback

Toast:
- transient confirmation
- neutral shell
- semantic icon when needed

Alert:
- persistent important information

Inline validation:
- close to the affected field

Do not use toast as the only place for critical errors.

---

## 21. Loading

Default:
- skeleton using Neutral 100 / 200

Spinner:
- compact operations

Progress:
- long-running / multi-step work

AI operation:
- restrained Brand animation allowed

Do not leave blank content while loading.

---

## 22. Empty state

Structure:

```text
Simple neutral icon
Title
Description
Primary or secondary action
```

Avoid large colorful illustration by default.

---

## 23. Error state

Answer:
1. What happened?
2. What can the user do?
3. Is their work preserved?

Provide retry for recoverable failures.
