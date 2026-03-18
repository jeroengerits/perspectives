---
name: jeroengerits-facts
description: "Use when a user needs the factual view inside jeroengerits-perspective or a standalone fact map. Acts as a required feedback provider by separating verified information, assumptions, and missing evidence."
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

## Trigger Signals

Use this skill when the task needs:

- a clean separation between verified facts and assumptions
- a list of constraints that materially affect the decision
- explicit unknowns that should block overconfidence
- clarity about what information should be gathered next

## Collaboration Contract

When used inside `jeroengerits-perspective`:

- this skill is a required feedback input
- return only factual material, assumptions, and unknowns
- avoid recommendation language
- label uncertainty clearly

When used alone:

- provide a concise fact map without trying to close the decision

## Input Contract

Expect a brief that includes:

- the decision, option, or plan being evaluated
- the available evidence or claims
- any stated constraints
- any obvious gaps in the current brief

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
- Label missing evidence clearly when a claim cannot be verified from the brief.

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
