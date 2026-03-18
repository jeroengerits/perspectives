# Perspectives

Structured decision skills for Codex.

`perspectives` is a small skill set for decisions that are too ambiguous, high-stakes, or contentious for a single blended answer. It keeps multiple lenses separate until synthesis, then turns them into one practical recommendation.

The repository contains one organizer skill, `perspective`, plus six supporting skills that analyze the same brief from different angles.

## Included Skills

- `perspective`: runs the full workflow and writes the final memo
- `facilitator`: frames the decision and structures synthesis
- `facts`: separates verified information, assumptions, and unknowns
- `feelings`: surfaces instinctive reactions and stakeholder sentiment
- `benefits`: argues the upside and value
- `risks`: pressure-tests downside and failure modes
- `ideas`: expands the option space with alternatives and mitigations

## How It Works

When you use `perspective`, it:

1. Normalizes the request into a decision brief.
2. Generates one internal clarifying question if the brief is incomplete.
3. Sends the clarifying question, when needed, to all six supporting skills.
4. Synthesizes an `Auto Answer` with assumptions labeled.
5. Dispatches the same normalized brief to all six supporting skills.
6. Preserves useful disagreement during synthesis.
7. Produces a decision memo with recommendation and next steps.
8. Appends the run to [`logs/perspective-runs.md`](logs/perspective-runs.md).

`perspective` always depends on all six supporting skills. It does not skip views.

## Output Shape

The default memo includes:

- `Decision`
- `Context`
- `Facts and Unknowns`
- `Emotional Signals`
- `Benefits`
- `Risks`
- `Alternatives`
- `Recommendation`
- `Next Steps`

## When To Use It

Good fit:

- choosing between real options
- evaluating proposals with meaningful tradeoffs
- stress-testing a plan before execution
- clarifying an ambiguous strategic problem
- generating alternatives before committing

Poor fit:

- simple factual lookup
- straightforward execution work
- coding tasks that need implementation rather than analysis
- trivial decisions where multiple lenses add no value

## Install

Install the organizer skill:

```bash
npx skills add https://github.com/jeroengerits/perspectives --skill perspective
```

Install a supporting skill the same way by replacing `perspective` with `facilitator`, `facts`, `feelings`, `benefits`, `risks`, or `ideas`.

Restart Codex after installing or updating a skill so the local skill set is reloaded.

## Usage

Use the full method:

```text
Use perspective to help me decide whether to launch this feature now or delay it by one sprint.

Objective: Improve activation without destabilizing onboarding.
Constraints: 2 engineers, limited analytics confidence, fixed release window.
Desired Output: A recommendation with tradeoffs and next steps.
```

Use a single lens directly:

```text
Use risks to pressure-test this rollout plan.
Use benefits to evaluate the upside of this proposal.
Use facts to separate facts, assumptions, and unknowns in this decision.
```

## Repository Layout

```text
.
├── benefits/
├── facilitator/
├── facts/
├── feelings/
├── ideas/
├── logs/
│   └── perspective-runs.md
├── perspective/
├── risks/
└── README.md
```

## Notes

- Skill definitions live in each `SKILL.md`.
- [`logs/perspective-runs.md`](logs/perspective-runs.md) is the append-only template and history file used by `perspective`.
- The method is intentionally opinionated: separate views first, synthesize second, and label assumptions explicitly.
