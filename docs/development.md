# Development Setup

This repository is documentation-first, so the environment setup is intentionally light. There is no runtime service to boot, but there is still a useful baseline setup for maintaining the repo cleanly.

## Prerequisites

Recommended tools:

- `git`
- `gh` for GitHub workflows
- a local Codex install if you want to test the skill in the real environment

Optional:

- another Git hosting remote instead of GitHub

## Clone the Repository

```bash
git clone https://github.com/Oleks1y/PragmaticAgent.git
cd PragmaticAgent
```

## Connect a Remote Repository

If the repository was created locally and you want to attach GitHub:

```bash
git init
git remote add origin https://github.com/<owner>/PragmaticAgent.git
git branch -M main
```

If you prefer SSH:

```bash
git remote add origin git@github.com:<owner>/PragmaticAgent.git
```

If you want a non-GitHub remote, the pattern is the same:

```bash
git remote add origin <your-remote-url>
```

Verify:

```bash
git remote -v
```

## GitHub Authentication

For GitHub CLI workflows:

```bash
gh auth login
gh auth status
```

Useful commands:

```bash
gh repo view
gh repo create
gh pr create
```

## Codex Skill Installation for Local Testing

To test the skill in your real Codex environment:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor
cp SKILL.md ~/.codex/skills/pragmatic-advisor/SKILL.md
mkdir -p ~/.codex/skills/pragmatic-advisor/docs
cp -R docs/* ~/.codex/skills/pragmatic-advisor/docs/
```

Optional compatibility assets:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor/agents
cp agents/pragmatic-advisor.md ~/.codex/skills/pragmatic-advisor/agents/pragmatic-advisor.md
```

If your Codex setup supports local agent profiles, you can also maintain a TOML profile under `~/.codex/agents/`.

## Suggested Maintenance Workflow

```bash
git pull --rebase
git checkout -b docs/update-pragmatic-agent
```

Make your edits, then:

```bash
git status
git add .
git commit -m "docs: update pragmatic agent guidance"
git push -u origin docs/update-pragmatic-agent
```

## What to Verify Before Publishing Changes

- links still point to real files
- examples are copy-pasteable
- install steps still match the current Codex layout
- the repository remains generic and does not drift into project-specific guidance

## No Extra Dependency Setup Required

At the moment, this repository does not require:

- a package manager
- a virtual environment
- build tooling
- runtime secrets

If that changes later, document it here rather than burying it in the README.

