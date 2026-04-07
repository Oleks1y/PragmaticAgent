# PragmaticAgent Codex-Native Design

## Problem

The original `pragmatic.md` agent is useful, but it is packaged as a single Claude-oriented agent prompt. That makes it easy to copy, but harder to install, discover, invoke consistently, and reuse inside Codex workflows.

## Goal

Create a Codex-native reusable repository that turns the "pragmatic technical sparring partner" concept into a skill-first package with:

- a clear `SKILL.md`
- explicit installation instructions
- example prompts and concrete use cases
- documentation that makes the skill easy to adopt and hard to misuse

## Constraints

- Keep the repository lightweight and documentation-first.
- Do not overbuild this into an MCP server, plugin runtime, or app.
- Preserve the spirit of the original agent: challenge assumptions, expose hidden cost, and prefer cheaper validation paths.
- Make the package native to Codex usage patterns rather than a raw prompt dump.

## Non-goals

- No automation, plugin runtime, or custom executable tooling.
- No speculative integrations with other agent platforms.
- No dependency on one project or domain.

## Recommended Packaging

The repository should be a skill-first package with this shape:

- `SKILL.md`: the reusable Codex instruction set
- `README.md`: repository landing page and positioning
- `.codex/INSTALL.md`: Codex-native install path
- `docs/install.md`: manual install and setup notes
- `docs/getting-started.md`: first successful invocation path
- `docs/use-cases.md`: scenario catalog
- `docs/examples.md`: copy-paste prompt examples and response patterns
- `docs/design-principles.md`: behavioral guardrails and philosophy
- `agents/pragmatic-advisor.md`: optional plain-prompt bridge for users who still want an agent-style file

## Skill Behavior

The skill should:

- challenge first, confirm second
- reject authority-only reasoning
- surface hidden assumptions
- make trade-offs explicit
- propose the cheapest useful experiment
- acknowledge when the original plan is already the right call

The skill should not:

- perform skepticism for theater
- block execution when the decision is low-risk and reversible
- invent objections to sound senior
- propose enterprise complexity as a default alternative

## Output Contract

To make the skill easy to use, its default response shape should be stable:

1. `What problem is actually being solved`
2. `Weak assumptions`
3. `Hidden costs`
4. `Cheaper path or simpler alternative`
5. `What to validate first`
6. `When the original plan is justified`

This makes the skill more operational than a personality prompt.

## Documentation Strategy

The repository front page should follow the broad pattern used by high-signal open-source repositories:

- strong title and one-sentence value proposition
- badges or compact metadata near the top
- short "why this exists" section
- quick start or installation path
- examples and docs navigation
- clear repo layout

For this repository, the README should optimize for quick comprehension by someone who lands on it cold from GitHub.

## Verification

Success is demonstrated by:

- a coherent Codex-native file structure
- copy-pasteable install and invocation instructions
- examples that clearly show how to call the skill
- documentation that explains when the skill should challenge and when it should accept

## Risks

- If the skill is too harsh, it becomes a blocker rather than a sparring partner.
- If it is too soft, it collapses into generic advice.
- If the docs are weak, the repo becomes another prompt dump instead of a reusable tool.
