# Perspectives

Structured multi-view decision skills for Codex.

`perspectives` is a small skill set for decisions that are too important, ambiguous, or high-friction for a single blended answer. Instead of collapsing everything into one voice, it separates the work into distinct lenses, then recombines them into one practical recommendation.

The repository contains one organizer skill, `perspective`, plus six specialist skills that analyze the same brief from different angles.

## Why This Exists

A lot of decisions fail for predictable reasons:

- facts and assumptions get mixed together
- risks dominate too early and kill exploration
- optimism hides operational constraints
- "strategy" becomes a vague summary instead of a decision
- nobody names what is still unknown

`perspective` exists to force discipline into that process.

It does that by making each lens explicit, collecting all six views on the same brief, preserving meaningful disagreement, and only then producing a recommendation.

## The Skills

### Organizer

- `perspective`: orchestrates the full method, normalizes the brief, collects all six supporting views, and produces the final memo

### Supporting Views

- `facilitator`: frames the decision, keeps the process structured, and provides the synthesis scaffold
- `facts`: separates verified information, assumptions, and unknowns
- `feelings`: surfaces instinctive reactions, stakeholder sentiment, and emotional signals
- `benefits`: argues the upside, leverage, and strategic value
- `risks`: pressure-tests downside, failure modes, and hard constraints
- `ideas`: expands the option space with alternatives, hybrids, and mitigations

## How The Method Works

When you use `perspective`, the organizer follows a strict workflow:

1. It decides whether the request is actually a decision, evaluation, or framing problem.
2. It rewrites the input into a neutral brief with objective, decision, scope, constraints, facts, open questions, and desired output.
3. If the brief is too vague, it generates exactly one internal clarifying question.
4. That question is analyzed by all six supporting skills.
5. The organizer synthesizes an `Auto Answer` and folds it back into the brief with assumptions labeled.
6. The full normalized brief is dispatched to all six supporting skills.
7. The organizer collects every response before writing the final output.
8. It preserves disagreement where that disagreement matters.
9. It produces a decision memo with recommendation and next steps.
10. It appends the full run to [`logs/perspective-runs.md`](logs/perspective-runs.md).

The important constraint is simple: `perspective` does not skip views. It always depends on `facilitator`, `facts`, `feelings`, `benefits`, `risks`, and `ideas`.

## What You Get Back

The default output is a decision memo with these sections:

- `Decision`
- `Context`
- `Facts and Unknowns`
- `Emotional Signals`
- `Benefits`
- `Risks`
- `Alternatives`
- `Recommendation`
- `Next Steps`

That shape is deliberate. It makes it harder to hide uncertainty, easier to inspect tradeoffs, and easier to act on the recommendation.

## Good Fit

Use `perspective` when you need structured thinking before committing:

- choosing between real options
- evaluating a proposal with meaningful tradeoffs
- stress-testing a plan before execution
- clarifying an ambiguous strategic problem
- generating alternatives before locking a direction
- producing a balanced decision memo for yourself or a team

## Poor Fit

Do not use this method for:

- simple factual lookup
- straightforward execution work
- implementation tasks that need code instead of analysis
- decisions so trivial that multiple lenses add no value

## Install

Install the organizer skill:

```bash
npx skills add https://github.com/jeroengerits/perspectives --skill perspective
```

Install any specialist the same way by replacing `perspective` with `facilitator`, `facts`, `feelings`, `benefits`, `risks`, or `ideas`.

After installing or updating a skill, restart Codex so it reloads the local skill set.

## How To Use It

### Use The Full Method

Use `perspective` when you want the full multi-view workflow:

```text
Use perspective to help me decide whether to launch this feature now or delay it by one sprint.

Objective: Improve activation without destabilizing onboarding.
Constraints: 2 engineers, limited analytics confidence, fixed release window.
Desired Output: A recommendation with tradeoffs and next steps.
```

### Use A Specialist Directly

Use an individual skill when you only want one lens:

```text
Use risks to pressure-test this rollout plan.
Use benefits to evaluate the upside of this proposal.
Use facts to separate facts, assumptions, and unknowns in this decision.
```

## Repository Structure

Each directory contains one skill definition:

```text
.
├── benefits/
├── facilitator/
├── facts/
├── feelings/
├── ideas/
├── perspective/
├── risks/
├── logs/
│   └── perspective-runs.md
└── README.md
```

## Design Principles

This repository is intentionally opinionated:

- keep views separate until synthesis
- preserve useful disagreement instead of forcing consensus
- label assumptions explicitly
- avoid false certainty when evidence is incomplete
- prefer a practical recommendation over a polished but empty summary

If the right answer is "delay, gather information, or run a smaller test," the method should say that directly.
