# PragmaticAgent

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111111)](./SKILL.md)
[![Docs](https://img.shields.io/badge/docs-ready-0a7f5a)](./docs/getting-started.md)
[![Focus](https://img.shields.io/badge/focus-pragmatic%20decisions-1f6feb)](./docs/use-cases.md)

Challenge technical plans before they harden into expensive mistakes.

`PragmaticAgent` is a Codex-native skill and documentation package for a pragmatic technical sparring partner: an agent that pressure-tests specs, architecture choices, feature ideas, and implementation plans without turning into a blocker.

It is designed for moments when "make it senior" is exactly the wrong instruction.

## Why This Exists

Many agent workflows fail in the same way:

- the user proposes a complex approach
- the model assumes the approach is already justified
- implementation starts before assumptions are checked
- the team pays for complexity it did not need

This repository exists to add a disciplined checkpoint before that happens.

The goal is not negativity. The goal is better decisions:

- challenge hype
- expose hidden cost
- propose cheaper paths
- keep good ideas moving

## How It Works

The workflow is intentionally simple:

1. Invoke the skill before implementation or commitment.
2. Give it the plan, spec, or proposal.
3. Let it pressure-test the reasoning, not just the wording.
4. Use the critique to cut scope, validate assumptions, or confirm the plan is already sound.

## What You Get

- a reusable `SKILL.md` for Codex
- an optional plain agent file for prompt-style workflows
- installation instructions for Codex usage
- example prompts you can copy directly into sessions
- use cases across architecture, infra, product, AI, and roadmap review
- clear behavioral guardrails so the agent stays pragmatic instead of performative

## Quick Start

1. Clone this repository.
2. Follow [`.codex/INSTALL.md`](./.codex/INSTALL.md).
3. In Codex, explicitly invoke the skill:

```text
Use skill `pragmatic-advisor`.

Review this proposal as a pragmatic technical sparring partner.
Challenge assumptions, identify hidden costs, and suggest a cheaper path if one exists.
Do not write code yet.
```

4. Paste your plan, spec, architecture, or idea.

## Example Prompts

Architecture review:

```text
Use skill `pragmatic-advisor`.

I want to split webhook processing into a new Go service with Kafka and Redis.
Review this proposal critically.
Tell me what assumptions I am making, what complexity I am buying, and what a cheaper path would be.
```

Feature sanity check:

```text
Use skill `pragmatic-advisor`.

I want to add an AI assistant that automatically fixes user configuration issues.
First tell me whether this is justified, what the hidden risks are, and what the smallest validating experiment is.
```

Spec pressure test:

```text
Use skill `pragmatic-advisor` before proposing implementation.

Below is my spec.
Your role is to challenge weak assumptions, flag over-engineering, and say clearly if the plan is already good.
```

More examples live in [docs/examples.md](./docs/examples.md).

## Documentation

- [Install](./docs/install.md)
- [Getting Started](./docs/getting-started.md)
- [Use Cases](./docs/use-cases.md)
- [Examples](./docs/examples.md)
- [Design Principles](./docs/design-principles.md)

## Repository Layout

- [`SKILL.md`](./SKILL.md): Codex-native reusable skill instructions
- [`agents/pragmatic-advisor.md`](./agents/pragmatic-advisor.md): optional prompt-file version
- [`.codex/INSTALL.md`](./.codex/INSTALL.md): Codex-oriented install instructions
- [`docs/install.md`](./docs/install.md): manual install and setup notes
- [`docs/getting-started.md`](./docs/getting-started.md): first successful workflow
- [`docs/use-cases.md`](./docs/use-cases.md): scenario catalog
- [`docs/examples.md`](./docs/examples.md): copy-paste prompts and expected behavior
- [`docs/design-principles.md`](./docs/design-principles.md): philosophy and guardrails

## What This Is Not

This repository is not:

- an MCP server
- a plugin runtime
- a framework for automatic blocking
- a generic "be negative" persona

If a proposal is already well-scoped and justified, the agent should say that and move on.

## Status

The repository is documentation-first and intentionally lightweight. The main asset is the skill itself plus the usage guidance that makes it reusable.

## Inspiration

The idea was inspired by the pragmatic agent pattern shared in the `extractum-skills` repository and adapted here into a Codex-native skill-first package with installation docs, examples, and a reusable GitHub home.
