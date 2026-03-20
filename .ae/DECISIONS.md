# Decisions

## [2026-03-20] AD-001: Pure Markdown & TOML Stack
- **Context**: Ae needs to be lightweight and portable without runtime dependencies.
- **Decision**: No JavaScript, Python, or Go. Use TOML for Gemini CLI command definitions and Markdown for state/context.
- **Rationale**: Minimalist, easy to read, and zero configuration for the end user.
