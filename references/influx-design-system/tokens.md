# Influx AI Design System — Tokens

## 1. Color primitives

### Neutral

```text
Neutral 0    #FFFFFF
Neutral 25   #FCFCFD
Neutral 50   #F8F8FA
Neutral 100  #F2F3F5
Neutral 200  #E7E8EC
Neutral 300  #D8DAE0
Neutral 400  #A9ADB8
Neutral 500  #7B8190
Neutral 600  #5E6472
Neutral 700  #404552
Neutral 800  #272B34
Neutral 900  #16181D
Neutral 950  #0B0C0F
```

### Influx Purple

```text
Brand 50   #F5F2FF
Brand 100  #ECE7FF
Brand 200  #D9D0FF
Brand 300  #BCAEFF
Brand 400  #947BFF
Brand 500  #6C47FF
Brand 600  #5B36F5
Brand 700  #4928D9
```

Default interactive brand color: Brand 500 / 600.

## 2. Semantic color tokens

Components should consume semantic tokens, not raw primitives.

```text
--bg-page              Neutral 25
--bg-surface           Neutral 0
--bg-subtle            Neutral 50
--bg-muted             Neutral 100

--text-primary         Neutral 900
--text-secondary       Neutral 600
--text-tertiary        Neutral 500
--text-disabled        Neutral 400
--text-inverse         Neutral 0

--border-subtle        Neutral 100
--border-default       Neutral 200
--border-strong        Neutral 300

--interactive-primary          Brand 600
--interactive-primary-hover    Brand 700
--interactive-primary-soft     Brand 50

--selected-bg           Brand 50
--selected-border       Brand 300
--selected-text         Brand 600
--focus-ring            Brand 100

--success               #1F8A4C
--success-soft          #EEF9F2
--warning               #B56A00
--warning-soft          #FFF7E8
--error                 #C63C3C
--error-soft            #FFF1F1
--info                  #3B6FD8
--info-soft             #EFF5FF
```

## 3. Spacing

Use a 4px grid.

```text
Space 1   4px
Space 2   8px
Space 3   12px
Space 4   16px
Space 5   20px
Space 6   24px
Space 8   32px
Space 10  40px
Space 12  48px
Space 16  64px
```

Recommended:
- icon-to-label: 8
- compact control gap: 8
- field group gap: 12–16
- card padding: 16 / 20 / 24
- section gap: 24 / 32
- major region gap: 40 / 48

Avoid arbitrary spacing such as 13, 17, 19, 27 unless required by an external embed.

## 4. Radius

```text
Radius XS   6px
Radius SM   8px
Radius MD   10px
Radius LG   12px
Radius XL   16px
```

Usage:
- tags/chips: 6
- buttons: 8
- inputs/selects: 8
- dropdowns: 10
- tables/cards: 12
- hero/modal: 16

Avoid excessive 20–24px radius on operational UI.

## 5. Borders

Default:
```text
1px solid Neutral 200
```

Hover:
```text
Neutral 300
```

Selected:
```text
Brand 300
```

## 6. Shadows

Default card:
```text
none
```

Floating surface:
```text
0 4px 12px rgba(0,0,0,0.06)
```

Modal / elevated overlay:
```text
0 8px 24px rgba(0,0,0,0.10)
```

Rule: if a border can solve it, do not add a shadow.

## 7. Motion

```text
Fast    120ms
Normal  180ms
Slow    240ms
```

Default easing:
```text
ease-out
```

Use motion for:
- hover
- focus
- dropdown
- popover
- modal
- drawer
- selected state

Do not add decorative motion merely to create an “AI feel”.

## 8. Z-index tiers

```text
Base content       0
Sticky header      10
Dropdown/popover   20
Drawer             30
Modal              40
Toast              50
```

Keep layering predictable.
