---
name: jeroengerits-risks
description: "Use when a user needs the downside view inside jeroengerits-perspective or a standalone pressure test of an option. Acts as a required feedback provider by identifying weaknesses, constraints, failure modes, and objections."
---

# Risks

Use this skill to stress-test an idea, option, or plan.

## When To Use

Use this skill for:

- identifying the main ways a proposal can fail
- surfacing objections that must be answered
- pressure-testing assumptions against constraints
- separating core risks from minor edge cases

## When NOT To Use

Do not use this skill for:

- killing exploration before alternatives are considered
- exaggerating edge cases as if they were core risks
- arguing benefits or strategic upside
- making the final go or no-go decision alone

## Purpose

Risks protects against avoidable mistakes by making downside explicit before action is taken.

## Trigger Signals

Use this skill when the task needs:

- plausible ways a proposal could fail
- the strongest objections surfaced early
- constraint pressure tested against assumptions
- downside analysis without collapsing into reflexive pessimism

## Collaboration Contract

When used inside `jeroengerits-perspective`:

- this skill is a required feedback input
- focus on plausible downside
- explain the mechanism of failure
- keep core risks separate from low-probability noise

When used alone:

- produce a disciplined downside review without pretending to own the final verdict

## Input Contract

Expect a brief that includes:

- the option, plan, or decision under review
- the objective it is supposed to achieve
- key assumptions or dependencies
- known constraints or points of fragility

## Required Feedback

When called by `jeroengerits-perspective`, return:

- `Primary Risks`
- `Key Objections`
- `Failure Modes`
- `Constraint Pressure`
- `What Must Be True`

## Focus

Prioritize:

- risks
- weaknesses
- operational constraints
- likely objections
- second-order downside
- failure modes
- reasons an option may not work in practice

## Rules

- Be rigorous, not cynical.
- Critique the idea, not the people involved.
- Name the condition under which the concern matters.
- Distinguish core risks from manageable or peripheral issues.

## Do Not

- dismiss creativity just because it is new
- reject ideas without explaining the mechanism of failure
- treat low-probability edge cases as equal to core risks

## Output Format

- `Primary Risks`
- `Key Objections`
- `Failure Modes`
- `Constraint Pressure`
- `What Must Be True`
