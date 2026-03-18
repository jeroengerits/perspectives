---
name: jeroengerits-perspective
description: "Use when a user needs a structured decision exercise, tradeoff analysis, or problem-framing pass with multiple views on the same problem. Acts as an organizer that always gathers feedback from jeroengerits-facilitator, jeroengerits-facts, jeroengerits-feelings, jeroengerits-benefits, jeroengerits-risks, and jeroengerits-ideas before producing one practical recommendation."
---

# Perspective

Use this skill when a user needs structured thinking for a decision, strategy, evaluation, tradeoff, or problem-framing exercise.

This skill is the organizer. It always gathers feedback from all six supporting skills, preserves useful disagreement, and produces the final recommendation.

## When To Use

Use this skill for:

- choosing between options
- stress-testing a proposal
- exploring upside and downside before acting
- framing an ambiguous problem
- generating alternatives before committing
- producing a balanced decision memo

## When NOT To Use

Do not use this skill for:

- straightforward factual lookups
- simple execution tasks with no real tradeoff
- situations where the user wants immediate implementation instead of analysis

## Trigger Signals

Use this skill when the user needs:

- a decision memo across competing viewpoints
- structured thinking before committing to a direction
- balanced treatment of upside, downside, evidence, sentiment, and alternatives
- help clarifying a messy decision before action

## Core Rule

Keep the views separate. Do not blend them into one generic analysis voice.

Each supporting skill has one clear job:

- `jeroengerits-facilitator` frames the process and synthesizes
- `jeroengerits-facts` states what is known, assumed, and missing
- `jeroengerits-feelings` surfaces instinctive reactions and sentiment
- `jeroengerits-benefits` explains upside and value
- `jeroengerits-risks` pressure-tests weaknesses and failure modes
- `jeroengerits-ideas` expands the option space with alternatives and reframes

## Organizer Rule

`jeroengerits-perspective` must always depend on all six supporting skills for feedback.

It must not skip a skill because a view seems obvious. It must not replace a role skill with its own inline opinion before collecting feedback.

## Input Contract

Build or request a brief with these fields:

- `Objective`
- `Decision`
- `Scope`
- `Constraints`
- `Known Facts`
- `Open Questions`
- `Desired Output`

If one or more fields are missing but the task is still clear enough to proceed, fill them in conservatively and label the assumptions.

If the decision itself is unclear, do not stop to ask the user first. Generate one concise random clarifying question internally, then run that question through all six supporting skills before continuing.

## Auto-Question Rule

When clarification is needed:

1. Generate exactly one concise random question that would materially improve the brief.
2. Treat that question as its own mini-brief.
3. Dispatch that same question-mini-brief to all six supporting skills:
   - `jeroengerits-facilitator`
   - `jeroengerits-facts`
   - `jeroengerits-feelings`
   - `jeroengerits-benefits`
   - `jeroengerits-risks`
   - `jeroengerits-ideas`
4. Collect all six responses before answering the question.
5. Synthesize one `Auto Answer` that explicitly labels assumptions.
6. Fold that `Auto Answer` back into the main brief before running the main analysis.

Do not answer the generated question from the organizer alone. Every generated question must be analyzed by all six supporting skills first.

## Workflow

1. Decide whether the request is actually a decision, evaluation, or framing problem.
2. Rewrite the request into a neutral brief:
   - objective
   - scope
   - constraints
   - decision to be made
   - desired output
3. If the brief is too vague, generate one concise random clarifying question internally.
4. Send that generated question to all six supporting skills and synthesize an `Auto Answer`.
5. Update the brief with the `Auto Answer` and any labeled assumptions.
6. Send the same main brief to all six supporting skills:
   - `jeroengerits-facilitator`
   - `jeroengerits-facts`
   - `jeroengerits-feelings`
   - `jeroengerits-benefits`
   - `jeroengerits-risks`
   - `jeroengerits-ideas`
7. Collect all six feedback responses before writing the final answer.
8. Preserve meaningful disagreement instead of forcing fake consensus.
9. Use `jeroengerits-facilitator` output to structure the synthesis, but keep all other views visible where they materially disagree.
10. Produce the default decision memo.
11. Append a full run log to `logs/perspective-runs.md`.

## Dispatch Rule

When dispatching the brief:

- send the same decision brief to every supporting skill
- require each skill to stay in role and use its own output format
- do not let one skill answer another skill's job
- treat missing or weak support-skill output as a reason to restate the brief, not as permission to skip the role
- apply the same dispatch rule to every generated clarifying question

## Execution

Always dispatch `jeroengerits-facilitator`, `jeroengerits-facts`, `jeroengerits-feelings`, `jeroengerits-benefits`, `jeroengerits-risks`, and `jeroengerits-ideas` with the same brief.

Require each supporting skill to return in-role feedback only.

If an auto-generated clarifying question was needed, dispatch those same six skills against that question first, then synthesize the `Auto Answer`, then run the main brief.

After all feedback is collected:

- use `jeroengerits-facilitator` for process framing and synthesis
- use `jeroengerits-facts` for evidence and unknowns
- use `jeroengerits-feelings` for instinctive signals
- use `jeroengerits-benefits` for upside
- use `jeroengerits-risks` for downside
- use `jeroengerits-ideas` for alternatives and mitigations

## Synthesis Rules

- Keep disagreement visible when it affects the recommendation.
- Explicitly mark where the recommendation depends on assumptions or missing evidence.
- Prefer a practical recommendation over a false sense of certainty.
- If the best answer is "delay, gather information, or run a smaller test," say that directly.

## Default Output Format

Produce a memo with these sections:

- `Decision`
- `Context`
- `Facts and Unknowns`
- `Emotional Signals`
- `Benefits`
- `Risks`
- `Alternatives`
- `Recommendation`
- `Next Steps`

## Quality Bar

The organizer must prevent these failure modes:

- skipping a view because it seems obvious
- mixing multiple views into one section
- presenting assumptions as facts
- synthesizing before all six skills respond
- letting `jeroengerits-risks` kill exploration too early
- letting `jeroengerits-benefits` become generic optimism
- letting `jeroengerits-ideas` ignore hard constraints
- hiding unresolved conflict inside a shallow summary

## Clarification Rule

If the user has not clearly defined the decision or problem, generate one concise random clarifying question internally, have all six supporting skills analyze it, synthesize an `Auto Answer`, and then continue the workflow.

If the request is not a good fit for Perspective, say so directly and explain what is missing or what simpler approach would be better.

## Logging Rule

For every run, append a Markdown entry to `logs/perspective-runs.md`.

Each log entry must include:

- `Timestamp`
- `Original Request`
- `Generated Question`
- `Question Analysis: Facilitator`
- `Question Analysis: Facts`
- `Question Analysis: Feelings`
- `Question Analysis: Benefits`
- `Question Analysis: Risks`
- `Question Analysis: Ideas`
- `Auto Answer`
- `Normalized Brief`
- `Main Analysis: Facilitator`
- `Main Analysis: Facts`
- `Main Analysis: Feelings`
- `Main Analysis: Benefits`
- `Main Analysis: Risks`
- `Main Analysis: Ideas`
- `Final Memo`

If no generated question was needed, still log `Generated Question` as `None` and `Auto Answer` as `Not needed`.
