# Getting Started

This guide is for the first successful use of `PragmaticAgent` in Codex.

## Step 1: Install the Skill

Follow [install.md](./install.md) or [`.codex/INSTALL.md`](../.codex/INSTALL.md).

## Step 2: Choose the Right Moment

Use the skill before commitment, not after:

- before a bug fix turns into a symptom patch
- before a small feature grows into a mixed refactor
- before adding a dependency
- before deciding what tests are enough
- before opening a large pull request
- before approving a spec
- before choosing new infrastructure
- before splitting into services
- before adding AI because it sounds powerful
- before roadmap items turn into implementation work

## Step 3: Invoke It Explicitly

Start with a direct prompt:

```text
Use skill `pragmatic-advisor`.

Review this proposal as a pragmatic technical sparring partner.
Challenge assumptions, identify hidden costs, and propose a cheaper path if one exists.
```

For ordinary engineering tasks, ask for a compact review:

```text
Use skill `pragmatic-advisor`.

Give me a 2-minute pragmatic review before I implement this.
Focus on scope, risk, simpler alternatives, and verification.
```

For architecture or high-risk decisions, ask for a full pressure test:

```text
Use skill `pragmatic-advisor`.

Give me a full pressure test before we commit to this design.
Challenge assumptions, hidden costs, reversibility, and validation.
```

## Step 4: Paste the Plan

Good inputs:

- bug fix plans
- small feature plans
- dependency choices
- test plans
- PR summaries
- specs
- architecture notes
- roadmap bullets
- "we should use X" proposals
- refactor plans
- infrastructure changes

## Step 5: Look for the Right Kind of Output

Good output looks like this:

- it questions the real problem
- it surfaces assumptions you skipped
- it explains hidden cost in practical terms
- it gives you a cheaper path or says the plan is already justified

Bad output looks like this:

- generic negativity
- obvious criticism with no alternative
- blanket rejection of all complexity
- "sounds good" without pressure-testing the plan

## A Good First Prompt

For everyday work:

```text
Use skill `pragmatic-advisor`.

I need to fix a bug where duplicate notifications are sent.
Before coding, tell me:
- what root cause I should verify
- what minimal fix would be enough
- what test would prove it
- what scope I should avoid expanding into
```

For strategic work:

```text
Use skill `pragmatic-advisor`.

I want to move background jobs into a separate worker service and add Redis.
Before we build anything, tell me:
- what problem I am really solving
- what assumptions I am making
- what extra operational cost this introduces
- what smaller path I should validate first
```

## A Good Follow-Up Prompt

```text
Use skill `pragmatic-advisor`.

I heard your critique.
Now tell me whether the original plan is still justified if these constraints are true:
- we process 2 million jobs per day
- queue latency is hurting SLAs
- the current monolith deploys too slowly
```

The skill should become more accepting when the evidence becomes stronger.
