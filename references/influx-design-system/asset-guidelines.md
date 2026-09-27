# Influx AI Design System — Asset Guidelines

## 1. Asset hierarchy

Preferred visual asset types, in order:

1. real product UI mock / product preview
2. creator photography
3. data visualization
4. simple line icon
5. illustration

Do not default to decorative illustration.

## 2. Creator photography

Style:
- photorealistic
- modern commercial creator aesthetic
- natural lighting
- realistic skin texture
- minimal or contextual background
- no watermark
- no visible brand logo unless intentionally representing a platform/product
- inclusive and globally relevant

Avoid:
- cyberpunk
- “AI glow”
- fantasy styling
- overly airbrushed skin
- dramatic editorial fashion unless relevant
- stock-photo clichés

## 3. Image ratios

### Avatar
```text
1:1
```

### Creator Card
```text
4:3
```

### Hero Creator Image
```text
4:5
```

### Wide Feature / Brand Card
```text
16:9 or 3:2
```

Use one ratio consistently within the same component type.

## 4. Safe area

Keep the important subject at least 12% away from crop boundaries when possible.

Do not place faces under:
- badges
- buttons
- platform logos
- metric overlays

## 5. AI-generated people

When generating people:
- use completely fictional subjects
- avoid resemblance to public figures
- use natural facial detail
- maintain realistic anatomy
- use age-appropriate styling
- avoid identifiable copyrighted fashion prints/logos

## 6. Creator card composition

Preferred:

```text
Image
Identity
Category tags
Key metrics
Primary / secondary action
```

Do not overload the image itself with many text overlays.

## 7. Hero composition

For AI Search hero / education panel:

- one dominant creator card
- one or two supporting creator cards
- official platform marks only
- minimal metric overlays
- subtle Brand 50/100 background motif
- sufficient whitespace

The visual should communicate:
```text
natural-language request
→ creator matching
→ useful creator data
```

Avoid random collage for decoration.

## 8. Icon system

Preferred icon family:
- Lucide or equivalent consistent outline family

Recommended:
```text
Stroke: 1.5–2px
Sizes: 16 / 18 / 20 / 24
```

Do not mix:
- outline
- filled
- 3D
- emoji
- multiple unrelated icon families

Official platform logos are exceptions.

## 9. Platform marks

Instagram, TikTok, YouTube may use official brand colors only in:
- logo mark
- platform identity
- creator source indicator

Do not propagate platform colors into:
- tabs
- backgrounds
- filters
- cards
- page chrome

## 10. Data visualization

Default:
- Neutral 200 / 300 for background or history
- Neutral 500 for secondary comparison
- Brand 500 for primary series
- semantic colors only for true positive/negative/error meaning

Avoid rainbow dashboards.

## 11. Image quality

Minimum:
- sharp enough for 2x display density
- no compression artifacts
- no obvious AI text artifacts
- consistent crop across repeated cards

For generated UI assets:
- design for the actual component ratio
- do not generate a random image and force-crop it later

## 12. Product screenshots / mockups

When showing product UI inside a hero:
- keep it legible
- simplify detail if reduced
- preserve consistent radius
- avoid perspective distortion unless subtle
- avoid more than 2–3 layered cards

## 13. Decorative gradients

Allowed only as restrained support:

```text
White → Brand 50
Neutral 25 → Brand 50
```

Do not use saturated multicolor gradients in standard product UI.

## 14. Asset generation prompt baseline

When generating creator imagery:

```text
Photorealistic fictional creator, modern commercial social-media aesthetic,
natural skin texture, realistic proportions, soft natural lighting,
clean contemporary composition, no visible logos, no watermark,
high detail, suitable for a premium SaaS creator-marketing product.
```

Then add:
- demographic
- pose
- crop
- outfit
- background
- aspect ratio

based on the specific component.
