# PragmaticAgent Codex-Native Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a reusable Codex-native repository for a pragmatic technical sparring partner skill, then publish it to GitHub as `PragmaticAgent`.

**Architecture:** Documentation-first repository with a reusable `SKILL.md` at the center, supported by install docs, examples, usage guidance, and an optional plain-agent bridge for compatibility with prompt-file workflows.

**Tech Stack:** Markdown, Git, GitHub, Codex skill conventions

---

## Chunk 1: Repository Initialization

### Task 1: Initialize and connect the repository

**Files:**
- Create: `.gitignore`
- Modify: git metadata only

- [ ] **Step 1: Verify the local directory is initialized as a git repository**

Run: `git status --short --branch`
Expected: git responds from this directory without "not a git repository"

- [ ] **Step 2: Create or connect the GitHub repository**

Run: `gh repo create Oleks1y/PragmaticAgent --public --source=. --remote=origin`
Expected: GitHub repo URL returned and `origin` configured

- [ ] **Step 3: Confirm the remote is configured**

Run: `git remote -v`
Expected: fetch and push URLs point to `Oleks1y/PragmaticAgent`

## Chunk 2: Core Skill Content

### Task 2: Create the reusable skill instructions

**Files:**
- Create: `SKILL.md`
- Create: `agents/pragmatic-advisor.md`

- [ ] **Step 1: Write the Codex-native skill contract**

Include:
- purpose
- when to use it
- response structure
- behavioral guardrails

- [ ] **Step 2: Add a compatibility plain-agent file**

Mirror the same intent in a compact agent-style format for users who prefer explicit prompt-file invocation.

- [ ] **Step 3: Review both files for tone drift**

Expected: critical but constructive, never theatrical

## Chunk 3: Repository Documentation

### Task 3: Create the public-facing documentation set

**Files:**
- Create: `README.md`
- Create: `.codex/INSTALL.md`
- Create: `docs/install.md`
- Create: `docs/getting-started.md`
- Create: `docs/use-cases.md`
- Create: `docs/examples.md`
- Create: `docs/design-principles.md`
- Create: `docs/repo-context.md`
- Create: `AGENTS.md`

- [ ] **Step 1: Write the landing page README**

Cover:
- what this is
- why it exists
- how to install
- how to use
- docs navigation

- [ ] **Step 2: Write installation docs**

Include Codex-native and manual install paths.

- [ ] **Step 3: Write example-driven usage docs**

Include architecture, product, AI, infra, and roadmap critique scenarios.

- [ ] **Step 4: Write repository context docs**

Document the repo role so future edits preserve reusability.

## Chunk 4: Verification and Publish

### Task 4: Verify repository quality and publish

**Files:**
- Modify: all created files as needed

- [ ] **Step 1: Review the repository tree**

Run: `find . -maxdepth 3 -type f | sort`
Expected: expected skill repo files are present

- [ ] **Step 2: Read key docs end-to-end**

Run: `sed -n '1,220p' README.md` and `sed -n '1,220p' SKILL.md`
Expected: install and usage flow are clear from cold start

- [ ] **Step 3: Review git diff for unnecessary scope**

Run: `git diff --stat` and `git diff --cached --stat`
Expected: only intended documentation/skill files changed

- [ ] **Step 4: Commit and push**

Run:
```bash
git add .
git commit -m "feat: add Codex-native pragmatic advisor skill"
git push -u origin main
```

Expected: branch published to GitHub
