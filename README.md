# Ae — Spec-Driven Development Framework

Ae is a development framework designed specifically for **Gemini CLI**, enabling a structured, persistent, and phase-based approach to building software.

## 🚀 The Core Idea
AI coding tools often lack long-term memory of a project’s lifecycle. **Ae** fixes this by introducing a spec-driven workflow where every decision, phase, and state is tracked in persistent Markdown and TOML files.

No runtime dependencies. No Node packages. No install scripts. Just pure intelligence and structured documentation.

## 🛠 Installation
Ae is distributed via Git. To use it in your project:

1. Clone this repository into your project's root:
   ```bash
   git clone https://github.com/aefjae/ae .ae_temp && mv .ae_temp/.gemini . && rm -rf .ae_temp
   ```
2. Run `/ae:new-project` in Gemini CLI to initialize the `.ae/` directory and `GEMINI.md` constitution.

## 🏗 The Build Flow
Ae follows a strict lifecycle for every feature or phase:

1.  **Research** (`/ae:research`): Gather context and investigate.
2.  **Initialize** (`/ae:new-project`): Define the Spec and Roadmap.
3.  **Discuss** (`/ae:discuss`): Clarify gray areas for a phase before planning.
4.  **Plan** (`/ae:plan`): Create a step-by-step implementation plan.
5.  **Execute** (`/ae:execute`): AI implements the planned changes.
6.  **Verify** (`/ae:verify`): Test and validate the implementation.
7.  **Review** (`/ae:review`): Perform a code review for quality assurance.
8.  **Ship** (`/ae:ship`): Finalize the phase and prepare for the next.

## 🕹 Commands Reference

| Command | Description |
| :--- | :--- |
| `/ae:new-project` | Initialize a new project with Ae structure (`SPEC.md`, `ROADMAP.md`, etc.). |
| `/ae:discuss` | Clarify gray areas for a phase before planning. |
| `/ae:plan` | Create detailed implementation plans for the current phase. |
| `/ae:execute` | Implement planned changes autonomously. |
| `/ae:verify` | Test and validate implementation against the plan. |
| `/ae:ship` | Finalize the current phase and update the roadmap. |
| `/ae:quick` | Handle small, atomic tasks without a full planning cycle. |
| `/ae:progress` | Display the current status of the project and its phases. |
| `/ae:next` | Identify the immediate next task or phase to tackle. |
| `/ae:research` | Conduct deep research or investigation before speccing. |
| `/ae:map` | Analyze an existing codebase to generate architectural context. |
| `/ae:review` | Perform a post-execution code review to ensure quality. |

## 📁 Project Structure
When initialized, Ae maintains your project state in the `.ae/` directory:
- `SPEC.md`: The source of truth for project requirements.
- `ROADMAP.md`: High-level phases and task tracking.
- `STATE.md`: Current phase and implementation status.
- `DECISIONS.md`: Log of architectural decisions and their rationale.
- `JOURNAL.md`: Session-by-session history of the project.

## 📄 License
MIT
