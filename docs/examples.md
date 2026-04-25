# Examples

These examples are meant to be copied into Codex with minimal editing.

## 1. Review a Bug Fix Before Coding

```text
Use skill `pragmatic-advisor`.

I need to fix this bug. Before coding, help me avoid a symptom patch.

Tell me:
- what root cause I should verify
- what minimal fix would be enough
- what test would prove it
- what scope I should not expand into

[describe bug here]
```

## 2. Keep a Small Feature Small

```text
Use skill `pragmatic-advisor`.

I am adding a small feature.
Give me a 2-minute pragmatic review focused on scope, risk, simpler implementation, and verification.

[describe feature here]
```

## 3. Check a Dependency Before Adding It

```text
Use skill `pragmatic-advisor`.

I am about to add a new dependency for this task.
Pressure-test whether it is worth it, what simpler option exists, and when the dependency would be justified.

Dependency:
Task:
Alternative I considered:
```

## 4. Review Pull Request Scope

```text
Use skill `pragmatic-advisor`.

Review this PR plan for scope.
Tell me what should stay, what should split out, what looks like unrelated cleanup, and what verification is enough.

[paste PR summary here]
```

## 5. Review a Test Plan

```text
Use skill `pragmatic-advisor`.

Review this test plan.
Tell me what behavior must be covered, what is overkill, and what manual verification remains.

[paste test plan here]
```

## 6. Critique an Architecture Idea

```text
Use skill `pragmatic-advisor`.

I want to move webhook ingestion into a separate Go service, add Kafka between ingestion and processing, and use Redis for retries.

Review this as a pragmatic technical sparring partner.
Do not write code.

Tell me:
- what problem I am actually solving
- what assumptions I am making
- what hidden cost I am buying
- what cheaper path I should validate first
- when this architecture would actually be justified
```

## 7. Check Whether a Product Feature Is Worth Building

```text
Use skill `pragmatic-advisor`.

I want to add an AI assistant that detects user configuration mistakes and auto-fixes them.

Pressure-test this idea before implementation.
I want a serious critique, not enthusiasm.
If the right answer is a smaller non-autonomous MVP, say so.
```

## 8. Review a Spec Before Coding

```text
Use skill `pragmatic-advisor` before proposing implementation.

Below is my spec.
Your role:
- challenge weak assumptions
- flag over-engineering
- point out hidden maintenance and ops cost
- say clearly if the spec is already good

[paste spec here]
```

## 9. Sanity-Check an Infra Decision

```text
Use skill `pragmatic-advisor`.

I want to add eBPF LSM support to control process behavior and network activity.

Review this from the perspective of install base, compatibility, operational complexity, and user value.
Tell me whether this is solving a real product problem or just buying sophistication.
```

## 10. Critique a Roadmap

```text
Use skill `pragmatic-advisor`.

Here is our roadmap for the next quarter.
I want you to identify:
- items with vague value
- hidden scope creep
- work that looks impressive but may not matter
- cheaper experiments or narrower MVP cuts

[paste roadmap here]
```

## 11. Ask for a More Accepting Second Pass

```text
Use skill `pragmatic-advisor`.

You already challenged this plan once.
Now reassess it using these additional facts:
- 80% of enterprise customers asked for it
- current support cost is high
- we already ran a manual pilot and it worked

Tell me whether the original plan is now justified.
```

## 12. Use the Plain Agent File Instead of the Skill

```text
Read `./agents/pragmatic-advisor.md` and follow it for this discussion.

I am considering a rewrite of our jobs subsystem.
Pressure-test that decision before we talk about implementation.
```
