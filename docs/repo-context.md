# Repository Context

This repository is the source of truth for the reusable `PragmaticAgent` Codex skill.

It owns:

- the reusable skill instructions
- the install and usage story
- the origin and workflow context for why this skill exists
- the example prompts and use-case catalog
- the repository framing for public GitHub consumption

It does not own:

- project-specific specs or plans
- company-specific architecture rules
- machine-specific Codex state
- automation or runtime tooling

## Maintenance Expectations

- Keep the repo generic and reusable.
- Favor clarity and practical examples over verbosity.
- Preserve the pragmatic tone: direct, useful, and non-theatrical.
- Preserve the contextual framing in `docs/origin-and-context.md` so the repo does not degrade into a generic contrarian prompt.
- Do not widen scope into plugins, servers, or automation unless a real need emerges.
