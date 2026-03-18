# Perspectives

Structured decision skills for Codex.

`perspectives` is a small skill set for decisions that are ambiguous, high-stakes, or contentious enough that a single blended answer is not useful. It keeps multiple lenses separate first, then turns them into one practical recommendation.

The repository contains one organizer skill, `perspective`, and six supporting skills that analyze the same brief from different angles.

## Skills

- `perspective`: orchestrates the full workflow and writes the final recommendation
- `facilitator`: frames the decision and structures the synthesis
- `facts`: separates verified information, assumptions, and unknowns
- `feelings`: surfaces instinctive reactions and stakeholder sentiment
- `benefits`: argues the upside and potential value
- `risks`: pressure-tests downside and failure modes
- `ideas`: expands the option space with alternatives and mitigations

## How It Works

When you use `perspective`, it:

1. Normalizes the prompt into a decision brief.
2. Produces one clarifying question if the brief is incomplete.
3. Shares the same clarified brief with all six supporting skills.
4. Preserves disagreement where it is informative.
5. Synthesizes the outputs into one recommendation with explicit assumptions and next steps.

`perspective` always depends on all six supporting skills.

## Output

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

Use it for:

- choosing between real options
- evaluating proposals with meaningful tradeoffs
- stress-testing a plan before execution
- clarifying an ambiguous strategic problem
- generating alternatives before committing

Do not use it for:

- simple factual lookup
- straightforward execution work
- coding tasks that need implementation rather than analysis
- trivial decisions where multiple lenses add no value

## Install

Install the organizer skill:

```bash
npx skills add https://github.com/jeroengerits/perspectives --skill perspective
```

Install a supporting skill the same way by replacing `perspective` with one of:

- `facilitator`
- `facts`
- `feelings`
- `benefits`
- `risks`
- `ideas`

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
├── perspective/
├── risks/
└── README.md
```

## Notes

- Skill definitions live in each `SKILL.md`.
- The method is intentionally opinionated: separate views first, synthesize second, and label assumptions explicitly.
