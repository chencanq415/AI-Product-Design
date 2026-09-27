# Influx AI Design System — AI Product Patterns

## 1. AI interface model

Every AI experience should visually distinguish:

### User Input
What the user asks or configures.

### System Configuration
Model, mode, data scope, filters, references.

### AI Output
Generated content, matches, analysis, recommendations.

### System State
Thinking, searching, generating, partial, failed, complete.

Do not visually blur these roles.

## 2. AI Search

Recommended structure:

```text
Prompt Composer
Platform / Scope
Primary Filters
Advanced Filters
Primary AI Action
Recent Searches
Preview / Education / Output
```

The control area should remain compact.

Recent history may be embedded beneath the controls when it supports fast reuse.

## 3. AI Prompt Composer

Prompt composer should:
- support multiline input
- preserve user text
- show optional attachments/references
- expose relevant AI mode only when needed
- keep advanced system configuration secondary

Do not overload the composer with many visible controls.

## 4. AI Action color

Brand Purple identifies core AI execution.

Examples:
- Search with AI
- Generate
- Analyze
- Rewrite with AI

Secondary AI controls remain neutral.

## 5. AI progress

Prefer meaningful states:
- Understanding request
- Searching creators
- Matching profiles
- Generating recommendations

Avoid fake deterministic percentages unless real progress data exists.

## 6. Streaming

When output streams:
- show content progressively
- allow Stop
- preserve partial content where useful
- avoid blocking the entire page

## 7. Retry / regenerate

Use explicit actions:
- Retry
- Regenerate
- Edit and rerun

Keep existing output accessible when possible.

## 8. AI errors

Differentiate:
- network error
- tool/data-source failure
- permission issue
- model failure
- partial completion

Tell the user what was preserved.

## 9. Human control

For actions that affect external systems:
- sending email
- publishing content
- contacting creators
- changing campaign status

AI may prepare or recommend, but user control should be explicit unless automation was intentionally configured.

## 10. AI Preview / Education panel

A right-side AI Search education panel may be more expressive than ordinary operational UI.

Allowed:
- very subtle Brand 50 gradient
- creator imagery
- platform marks
- light data cards
- small decorative AI motif

Still avoid:
- heavy saturated gradient
- multiple decorative colors
- oversized empty hero
- excessive card tilt / 3D effects

The panel should explain value, not distract from the task.
