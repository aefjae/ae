# Ae — Project Intelligence Layer

You are operating under the **Ae** spec-driven development framework.

## Core Rules (never break these)
- Never write code before a SPEC.md exists and is marked `status: FINALIZED`
- Never start a phase before its CONTEXT.md and PLAN.md exist
- After every meaningful action, update `.ae/STATE.md`
- Every task gets its own atomic git commit — no bundling unrelated changes
- Never skip `/ae:verify` — untested phases don't get marked complete

## State Files
- `.ae/SPEC.md` — the finalized project spec. Source of truth.
- `.ae/ROADMAP.md` — phases, tasks, completion status
- `.ae/STATE.md` — current phase, last command run, blockers
- `.ae/DECISIONS.md` — architecture decisions with rationale
- `.ae/JOURNAL.md` — append-only session log

## Commit Format
`[ae] phase-N: short description of what changed`
For quick tasks: `[ae:quick] short description`

## When in doubt
Read `.ae/STATE.md` first. It tells you where you are.