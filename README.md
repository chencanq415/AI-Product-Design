# AI Product Design

AI Product Design is a product-thinking copilot. It helps product managers, designers, founders, and AI coding workflows improve an idea through a focused conversation before turning it into a deliverable.

It is not a one-shot product-spec generator. By default, it challenges the current proposal, identifies the next decision, and advances one design layer at a time. A full PRD, implementation prompt, final solution, or visual-direction prompt is created only when the user explicitly asks for one.

## What it helps with

- Clarifying the actual product problem behind a feature request
- Separating known facts, assumptions, constraints, and unresolved decisions
- Stress-testing product logic and existing page structures
- Shaping information architecture, flows, interactions, and visual language in sequence
- Giving 2–3 useful directions when a real trade-off remains
- Converting agreed decisions into a PRD, implementation prompt, final proposal, or visual brief on request

## Default workflow

```text
Current idea
  -> Diagnose gaps and conflicts
  -> Advance one decision layer
  -> User feedback
  -> Refine and advance
  -> Explicit request for final artifact
  -> PRD / prompt / final proposal / visual brief
```

The normal sequence is:

```text
Problem definition
  -> User and scenario
  -> Information architecture
  -> Core flow
  -> Interaction details
  -> Visual language
```

The skill does not mechanically interrogate the user. When the information for a layer is already available, it analyzes and advances instead of asking redundant questions.

## Core behavior

The skill first understands the user's current idea, goal, constraints, and any existing page or plan. It then calls out the gaps that actually matter: a vague user, a feature that does not solve the stated problem, a conflict with technical limits, an overloaded navigation model, or an unresolved ownership/state decision.

Each response is deliberately narrow. It either delivers a phase-level analysis or presents up to three consequential options, then waits for the user to steer the next turn. It should be decisive when evidence supports a recommendation, and challenging when the proposal is weak—without inventing questions for the sake of asking them.

Routine UI choices are inferred from mature patterns unless they change business logic, permissions, data, core workflow, irreversibility, technical feasibility, or major information architecture.

## Final delivery is opt-in

The skill switches to final-delivery mode only when the user clearly says something equivalent to:

- “整理成 prompt”
- “输出 PRD”
- “给最终方案”
- “生成视觉稿指令”
- “可以直接做了”

At that point, it summarizes the decisions and remaining assumptions, then produces the requested artifact. It does not assume that a detailed final answer is wanted merely because the topic is complex.

## Example: a multi-turn refinement

### Turn 1 — user

> We want an AI search workspace. People can start a conversation, configure parameters, and see history. Keep the existing sidebar and top navigation.

### Turn 1 — skill

> The request bundles three different jobs: starting research, controlling answer quality, and returning to prior work. The unresolved product decision is whether parameters are a per-conversation setup or a global preference; that changes both history meaning and the main workspace layout.
>
> I recommend per-conversation settings: they preserve experiment context and make history useful. Before designing the layout, confirm one thing: are users comparing several search runs in one workspace, or is each conversation a single linear research thread?

### Turn 2 — user

> Mostly a single linear research thread, but users often try a different model after a poor answer.

### Turn 2 — skill

> Then do not make model choice a global setting. Treat it as a run-level control inside one conversation: the thread remains the container, while each answer records its model and relevant settings. This avoids fragmenting history every time someone retries.
>
> The next layer is information architecture. Two viable directions:
>
> 1. **Inline controls above the composer** — fastest for frequent model changes; less room for advanced settings.
> 2. **Compact settings panel beside the conversation** — keeps the composer focused; stronger when settings include sources, depth, and output format.
>
> Choose inline controls if the only frequent decision is model. Choose the panel if users regularly tune more than two inputs.

### Turn 3 — user

> Use the compact panel. Settings are model, source scope, and answer depth. Now give me the final implementation prompt.

### Turn 3 — skill

> The user explicitly requests a final artifact, so the skill switches to final-delivery mode. It summarizes the agreed thread/run model and creates a self-contained implementation prompt rather than reopening the earlier decisions.

## Repository structure

```text
AI-Product-Design/
├── SKILL.md
├── README.md
└── references/
    └── design-system.md
```

`SKILL.md` contains the collaboration model, stage rules, and explicit final-delivery triggers. `references/design-system.md` is consulted only when the conversation reaches visual language and no stronger existing system applies.
