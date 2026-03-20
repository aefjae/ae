# Project Spec
status: FINALIZED

## Summary
Ae is a spec-driven development framework for Gemini CLI — a set of slash commands that guide an AI through planning and building software projects phase by phase.

## Problem
AI coding tools like Gemini CLI have no memory of what you're building — every session starts from zero. Ae gives it persistent context, a spec, and a phase-by-phase plan so it always knows what to build next.

## Target User
Solo developers who use Gemini CLI and want a more structured, persistent development workflow.

## V1 Features (in scope)
- `/ae:new-project`: Initialize a new project with Ae structure.
- `/ae:discuss`: Research and discuss requirements.
- `/ae:plan`: Create detailed implementation plans.
- `/ae:execute`: Implement planned changes.
- `/ae:verify`: Test and validate implementations.
- `/ae:ship`: Finalize and prepare for delivery.
- `/ae:quick`: Handle small, atomic tasks.
- `/ae:progress`: Show current status of the project.
- `/ae:next`: Identify the next task or phase.
- `/ae:research`: Deep research before speccing.
- `/ae:map`: Analyze existing codebases.
- `/ae:review`: Post-execution code review.

## Out of Scope
- GUI or web dashboard.
- Multi-user support or cloud sync.
- Runtime dependencies beyond Gemini CLI (no Node packages, no install scripts).
- Distributed via git clone, pure TOML and Markdown.

## Stack
- Pure TOML (for command definitions)
- Markdown (for state and documentation)
- Developed in GitHub Codespaces
- Distributed via Git
