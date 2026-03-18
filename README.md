# Perspectives

Operational skill set for structured decision-making in Claude Code.

This repository contains one organizer skill, `jeroengerits-perspective`, and six supporting role skills that force a decision through distinct lenses before producing a recommendation.

## What This Is

Use this repository when a problem benefits from deliberate multi-view analysis instead of a single blended response.

The method separates:

- process and synthesis
- facts and unknowns
- feelings and instinctive reactions
- benefits and upside
- risks and downside
- ideas and alternatives

The goal is simple: make better decisions by preventing one mode of thinking from dominating too early.

## Primary Entrypoint

Start with `jeroengerits-perspective`.

That organizer skill:

- determines whether the request is actually a good fit for structured decision work
- rewrites the request into a neutral brief
- dispatches the same brief to all six supporting skills
- waits for all six responses
- synthesizes one practical recommendation while preserving meaningful disagreement

Do not start with the specialist skills unless you explicitly want only one lens.

## Supporting Skills

### `jeroengerits-facilitator`

Frames the decision, defines scope and constraints, preserves tension, and returns synthesis scaffolding.

### `jeroengerits-facts`

Separates verified facts, assumptions, unknowns, and information gaps.

### `jeroengerits-feelings`

Surfaces instinctive reactions, hesitation, enthusiasm, and likely stakeholder sentiment.

### `jeroengerits-benefits`

Builds the strongest concrete case for upside, value creation, leverage, and strategic fit.

### `jeroengerits-risks`

Pressure-tests failure modes, objections, fragility, and constraint pressure.

### `jeroengerits-ideas`

Generates alternatives, reframes, combinations, and mitigations before the decision closes.

## Workflow

The intended flow is:

1. Decide whether the request is a real decision, tradeoff, or framing problem.
2. Build a neutral brief with objective, decision, scope, constraints, known facts, open questions, and desired output.
3. Send that same brief to all six supporting skills.
4. Collect all six responses before synthesizing.
5. Produce a decision memo with a recommendation and next steps.

The organizer should not skip a role because the answer seems obvious.

## When To Use

Use `jeroengerits-perspective` for:

- choosing between options
- evaluating proposals with real tradeoffs
- stress-testing a plan before acting
- clarifying an ambiguous problem
- generating alternatives before commitment

## When Not To Use

Do not use this method for:

- straightforward factual lookup
- simple execution with no real decision
- tasks where the user wants immediate implementation instead of analysis

## Repository Structure

```text
.
├── benefits/
│   └── SKILL.md
├── facilitator/
│   └── SKILL.md
├── facts/
│   └── SKILL.md
├── feelings/
│   └── SKILL.md
├── ideas/
│   └── SKILL.md
├── perspective/
│   └── SKILL.md
└── risks/
    └── SKILL.md
```

## Example Use

Example prompt for the organizer:

```text
Use jeroengerits-perspective to help me decide whether to launch this feature now or delay it by one sprint. The objective is to improve activation without destabilizing onboarding. Current constraints: 2 engineers, limited analytics confidence, and a fixed release window.
```

If the request is too vague, the organizer should ask one concise clarifying question before dispatching the workflow.
