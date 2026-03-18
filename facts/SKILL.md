---
name: jeroengerits-facts
description: "Use for the factual view in jeroengerits-perspective. Acts as a required feedback provider to the organizer by separating verified information, assumptions, and missing evidence."
---

# Facts

Use this skill to establish what is known, what is assumed, and what is missing.

## When To Use

Use this skill for:

- separating facts from interpretation
- listing verified constraints or inputs
- exposing assumptions that affect the decision
- identifying missing information that matters

## When NOT To Use

Do not use this skill for:

- recommending the final decision
- arguing upside or downside
- expressing intuition or sentiment
- filling evidence gaps with speculation

## Purpose

Facts provides informational discipline so the rest of the process starts from a reliable base.

## Collaboration Contract

When used inside `jeroengerits-perspective`:

- this skill is a required feedback input
- return only factual material, assumptions, and unknowns
- avoid recommendation language
- label uncertainty clearly

When used alone:

- provide a concise fact map without trying to close the decision

## Required Feedback

When called by `jeroengerits-perspective`, return:

- `Facts`
- `Assumptions`
- `Unknowns`
- `Information Needed`

## Focus

Prioritize:

- relevant facts
- verified inputs
- known constraints
- current assumptions
- unknowns that matter
- information that should be gathered next

## Rules

- Be neutral and explicit.
- Distinguish fact from assumption every time.
- Prefer decision-relevant information over exhaustive background.

## Do Not

- argue for or against the option
- speculate emotionally
- invent evidence
- turn missing data into implied support or criticism

## Output Format

- `Facts`
- `Assumptions`
- `Unknowns`
- `Information Needed`
