# PragmaticAgent Install for Codex

This repository is meant to be used as a reusable Codex skill package.

## Fast Path

If this repository is already cloned locally, tell Codex:

```text
Follow the install instructions in /path/to/PragmaticAgent/.codex/INSTALL.md
```

Then ask it to install the skill into your Codex skills directory.

## Manual Install

1. Clone this repository somewhere stable on your machine.
2. Create a target skill directory:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor
```

3. Copy the skill file:

```bash
cp /path/to/PragmaticAgent/SKILL.md ~/.codex/skills/pragmatic-advisor/SKILL.md
```

4. Optional but recommended: copy the docs with it so the skill has local reference material:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor/docs
cp -R /path/to/PragmaticAgent/docs/* ~/.codex/skills/pragmatic-advisor/docs/
```

## First Use

Invoke the skill explicitly:

```text
Use skill `pragmatic-advisor`.

Review this plan as a pragmatic technical sparring partner.
Do not write code yet.
Challenge assumptions, flag hidden costs, and tell me whether a cheaper path exists.
```

## Recommendation

Treat this skill as a pre-implementation filter:

- before architecture work
- before introducing new infra or dependencies
- before turning a feature idea into a build commitment
- before accepting a "senior-looking" plan at face value

