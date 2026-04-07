# AGENTS.md

Before editing this repository, read these files in order:

1. `docs/repo-context.md`
2. `docs/origin-and-context.md`
3. `README.md`
4. `SKILL.md`
5. `docs/install.md`

## Repository Role

This repository is the source of truth for the reusable `PragmaticAgent` Codex skill.

It owns:

- reusable skill instructions
- Codex-first install and usage guidance
- example prompts and use-case docs

It does not own:

- project-specific outputs
- one team's internal process rules
- executable automation systems

## Required Behavior

- Keep this repo generic and reusable.
- Preserve the skill's core behavior: challenge weak assumptions without becoming a blocker.
- Keep examples concrete and copy-pasteable.
- Avoid unnecessary infrastructure, runtime code, or plugin scope.
