# Origin and Context

This repository did not start as a generic "critical reviewer" prompt.

It started from a specific need: most agent-assisted planning fails not because the model cannot generate ideas, but because it agrees too early with plans that sound impressive, senior, or sophisticated.

## The Problem This Repository Addresses

In practical development workflows, a common failure mode looks like this:

- a spec is too optimistic
- an architecture idea is accepted before assumptions are checked
- operational and maintenance costs stay implicit
- "best practice" language replaces evidence
- implementation starts before anyone asks whether a cheaper path exists

The result is not always a broken system. More often it is a system that technically works while costing more than the underlying problem justified.

## The Intended Role of PragmaticAgent

`PragmaticAgent` exists to act as a pragmatic technical sparring partner before commitment.

It is meant to be used:

- before ordinary tasks grow beyond their actual problem
- before bug fixes patch symptoms instead of causes
- before pull requests become hard to review
- before dependencies are added for small jobs
- before architecture decisions harden
- before new infrastructure is introduced
- before a roadmap item becomes a build commitment
- before "make it more senior" turns into accidental over-engineering

It is not meant to replace implementation, code review, product management, or final decision-making. Its role is narrower and more practical:

- challenge assumptions
- surface hidden cost
- force trade-offs into the open
- suggest smaller validation steps
- confirm when the current plan is already justified

## Why Codex-Native Packaging Matters

The original inspiration came from a single agent prompt file. That format is useful for quick copying, but weak as a reusable tool:

- install and invocation are ambiguous
- examples are usually missing
- behavior is easy to misread as "be harsh"
- there is no durable repository context for future maintenance

This repository packages the idea natively for Codex so it becomes:

- installable
- easier to invoke consistently
- documented with concrete examples
- maintainable as a public artifact

## What "Context" Means Here

For this repository, context includes:

- the problem pattern the skill is designed to counter
- the intended place of the skill in a development workflow
- the difference between constructive pressure-testing and generic negativity
- the design choice to keep this repo lightweight and documentation-first

That context matters because without it, the skill can easily drift into the wrong behavior:

- becoming a blocker
- sounding cynical instead of practical
- criticizing everything equally
- losing the distinction between reversible and expensive-to-reverse decisions

## Behavioral Boundary

The repository is explicitly optimizing for a specific kind of critique:

- direct, not theatrical
- pragmatic, not performatively skeptical
- evidence-seeking, not authority-seeking
- scope-reducing, not scope-expanding

If this skill ever starts sounding like a generic contrarian persona, it is drifting away from the repository's purpose.

## Recommended Place in the Workflow

The best place to use `PragmaticAgent` is between task intent and implementation.

Typical sequence:

1. Describe the bug fix, feature, PR, dependency, proposal, or spec.
2. Invoke `pragmatic-advisor` to pressure-test it.
3. Cut scope, validate assumptions, or confirm the plan.
4. Only then move into implementation planning or coding.

This is the main workflow context the repository is built around.

## Adaptation Notes

The repository was shaped to preserve the spirit of the original pragmatic-agent idea while adapting it for Codex:

- `SKILL.md` is the main reusable instruction asset.
- `README.md` is the public GitHub landing page.
- docs provide installation, use cases, and copy-paste prompts.
- the plain agent file remains available only as a compatibility bridge.

The repository should keep this structure unless there is a strong reason to change it.
