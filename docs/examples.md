# Examples

These examples are meant to be copied into Codex with minimal editing.

## 1. Critique an Architecture Idea

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

## 2. Check Whether a Feature Is Worth Building

```text
Use skill `pragmatic-advisor`.

I want to add an AI assistant that detects user configuration mistakes and auto-fixes them.

Pressure-test this idea before implementation.
I want a serious critique, not enthusiasm.
If the right answer is a smaller non-autonomous MVP, say so.
```

## 3. Review a Spec Before Coding

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

## 4. Sanity-Check an Infra Decision

```text
Use skill `pragmatic-advisor`.

I want to add eBPF LSM support to control process behavior and network activity.

Review this from the perspective of install base, compatibility, operational complexity, and user value.
Tell me whether this is solving a real product problem or just buying sophistication.
```

## 5. Critique a Roadmap

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

## 6. Ask for a More Accepting Second Pass

```text
Use skill `pragmatic-advisor`.

You already challenged this plan once.
Now reassess it using these additional facts:
- 80% of enterprise customers asked for it
- current support cost is high
- we already ran a manual pilot and it worked

Tell me whether the original plan is now justified.
```

## 7. Use the Plain Agent File Instead of the Skill

```text
Read `./agents/pragmatic-advisor.md` and follow it for this discussion.

I am considering a rewrite of our jobs subsystem.
Pressure-test that decision before we talk about implementation.
```

