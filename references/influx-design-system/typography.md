# Influx AI Design System — Typography

## Font family

Preferred:
- Inter
- SF Pro on Apple platforms
- system-ui fallback

Web stack:

```css
font-family:
  Inter,
  -apple-system,
  BlinkMacSystemFont,
  "Segoe UI",
  sans-serif;
```

## Font weights

Use only:
- 400 Regular
- 500 Medium
- 600 Semibold

Avoid 700–900 unless required for a rare marketing headline.

## Type scale

### Display

```text
32px / 40px
Weight 600
```

Use only for:
- onboarding
- marketing hero
- AI introduction panels

### Page Title

```text
24px / 32px
Weight 600
```

Examples:
- Creator Marketplace
- Outreach
- AI Tools

### Section Title

```text
18px / 26px
Weight 600
```

Examples:
- Recent Searches
- Email Sequence
- Audience Insights

### Card / Panel Title

```text
16px / 24px
Weight 600
```

### Body

```text
14px / 22px
Weight 400
```

Default UI content.

### Body Strong

```text
14px / 22px
Weight 500
```

Use for:
- creator name
- row primary value
- active label
- field value

### Secondary

```text
13px / 20px
Weight 400
```

Use for supporting description.

### Caption

```text
12px / 18px
Weight 400
```

Use for:
- metadata
- timestamp
- helper text
- secondary metrics

### Micro

```text
11px / 16px
Weight 500
```

Use sparingly:
- table header
- tiny chart label
- small status label

## Typography rules

1. Do not use color alone to establish hierarchy.
2. Prefer weight + spacing before increasing font size.
3. Use sentence case for UI labels.
4. Avoid uppercase except very small metadata headers.
5. Keep titles concise.
6. Do not mix many weights in the same component.
7. Use tabular numerals for dense data tables where supported.

## Text color mapping

```text
Primary content     Neutral 900
Secondary content   Neutral 600
Tertiary metadata   Neutral 500
Placeholder         Neutral 400
Disabled            Neutral 400
Link / selected     Brand 600
```

## Truncation

Single-line table fields:
- truncate with ellipsis
- provide tooltip only when full value matters

Long descriptions:
- allow 2–3 lines in cards
- do not expand card height unpredictably unless content reading is the task
