# Everyday Workflows

`PragmaticAgent` is useful for big architecture calls, but its highest-frequency value is ordinary engineering judgment.

Use it when a task feels small but still has room to grow in the wrong direction.

## 1. Bug Fix Sanity Check

Use before writing the fix when the root cause is not proven.

Prompt:

```text
Use skill `pragmatic-advisor`.

I need to fix this bug.
Give me a compact pragmatic review:
- likely root cause to verify
- minimal fix
- test that proves the fix
- scope I should avoid
```

Good outcome:

- root cause is checked before implementation
- the fix stays narrow
- the regression test targets the changed behavior

## 2. Small Feature Scope Check

Use when a small feature starts pulling in cleanup, abstractions, or adjacent behavior.

Prompt:

```text
Use skill `pragmatic-advisor`.

I am adding this small feature.
Check whether the scope is still proportional and what I should defer.

[describe feature]
```

Good outcome:

- the feature remains reviewable
- unrelated cleanup is deferred
- the smallest useful version is clear

## 3. Pull Request Size Review

Use before opening a PR or when a PR starts feeling hard to review.

Prompt:

```text
Use skill `pragmatic-advisor`.

Review this PR plan for scope.
Tell me what should stay, what should split out, and what verification is enough.

[paste PR summary]
```

Good outcome:

- functional changes are separated from cleanup when needed
- review risk is reduced
- verification maps to the real behavior changed

## 4. Dependency Check

Use before adding a package, service, framework, or tool.

Prompt:

```text
Use skill `pragmatic-advisor`.

I am about to add this dependency.
Pressure-test whether it is worth it.

Dependency:
Problem:
Alternatives considered:
```

Good outcome:

- the dependency solves a real problem
- simpler built-in options are considered
- long-term maintenance cost is visible

## 5. Refactor Review

Use when "while I am here" starts expanding the task.

Prompt:

```text
Use skill `pragmatic-advisor`.

I want to refactor this area while implementing a change.
Tell me whether the refactor reduces risk or just expands scope.
```

Good outcome:

- local simplification is allowed
- broad rewrites are challenged
- refactor work has a direct reason

## 6. Test Plan Review

Use when you are unsure how much testing is enough.

Prompt:

```text
Use skill `pragmatic-advisor`.

Review this test plan.
Tell me what behavior must be covered, what is overkill, and what manual verification remains.
```

Good outcome:

- tests cover the behavior that changed
- low-value test bulk is avoided
- manual verification is explicit when automation is missing

## 7. Daily Decision Rule

For everyday tasks, ask for a short answer unless the risk is high:

```text
Use skill `pragmatic-advisor`.

Give me a 2-minute pragmatic review.
Keep it short unless there is a serious hidden risk.
```

The skill should help preserve momentum, not turn every small task into an architecture review.

