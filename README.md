# Perspectives

Opinionated multi-view decision skills for Codex.

This repository contains one organizer skill, `perspective`, and six supporting skills that analyze the same decision from different angles before producing a recommendation.

## Roles

- `perspective`: organizer and final synthesis
- `facilitator`: frame the decision and structure the synthesis
- `facts`: separate facts, assumptions, and unknowns
- `feelings`: surface instinctive reactions and stakeholder sentiment
- `benefits`: argue the upside and value
- `risks`: pressure-test downside and failure modes
- `ideas`: generate alternatives, hybrids, and mitigations

## How It Works

Use `perspective` when you want structured thinking instead of a single blended answer.

The organizer:

1. rewrites the request into a neutral brief
2. if needed, generates one internal random clarifying question
3. sends that question to all six supporting skills
4. synthesizes an `Auto Answer`
5. sends the normalized brief to all six supporting skills
6. produces the final decision memo
7. appends the run to `logs/perspective-runs.md`

## When To Use

Good fit:

- choosing between options
- evaluating a proposal with real tradeoffs
- stress-testing a plan
- clarifying an ambiguous problem
- generating alternatives before committing

Not a good fit:

- simple factual lookup
- straightforward execution tasks
- requests that need implementation instead of analysis

## Install

```bash
npx skills add https://github.com/jeroengerits/perspectives --skill perspective
```

Install a specialist the same way by replacing `perspective` with `facilitator`, `facts`, `feelings`, `benefits`, `risks`, or `ideas`.

After installing or updating a skill, restart Codex so it reloads the local skill set.

## Prompts

Basic organizer prompt:

```text
Use perspective to help me decide whether to launch this feature now or delay it by one sprint. The objective is to improve activation without destabilizing onboarding. Current constraints: 2 engineers, limited analytics confidence, and a fixed release window.
```

Auto-question and logging prompt:

```text
Use perspective to analyze this request. If the brief is unclear, generate exactly one random clarifying question internally. Have that question analyzed by all six skills: facilitator, facts, feelings, benefits, risks, and ideas. Synthesize those six outputs into an Auto Answer with assumptions clearly labeled. Then run the full normalized brief through the same six skills, produce the final decision memo, and append the full run to logs/perspective-runs.md.

Request: [replace this with the actual decision or problem]
```

Use a specialist directly when you only want one lens:

```text
Use risks to pressure-test this rollout plan.
Use benefits to evaluate the upside of this proposal.
Use facts to separate facts, assumptions, and unknowns in this decision.
```
