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

## Anti-Patterns (never do these)
- Never hand a task back to the user with "you should..." — complete it or ask one specific blocking question
- Never assume package versions — run /ae:versions first before adding any dependency
- Never continue after 3 failed attempts on the same issue — run /ae:checkpoint and report
- Never generate more than 2 new files for a simple task — question complexity first
- Never lose thread across long tasks — checkpoint every phase completion

## Loop Detection
- If you notice you're repeating the same approach, stop immediately
- State what you've tried (max 3 attempts logged)
- Propose a different approach
- Ask user to confirm before proceeding

## Session Start Protocol
- Every new session: read .ae/STATE.md first
- If a checkpoint exists in .ae/checkpoints/, run /ae:resume before anything else

## Commit Format
`[ae] phase-N: short description of what changed`
For quick tasks: `[ae:quick] short description`

## When in doubt
Read `.ae/STATE.md` first. It tells you where you are.