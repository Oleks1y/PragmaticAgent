# Use Cases

`PragmaticAgent` is useful whenever a plan may be buying more complexity than the problem requires.

It covers both ordinary engineering tasks and larger strategic decisions.

## 1. Everyday Bug Fix Review

Example:

- "Let's patch this by adding a fallback."
- "The error is gone if we retry three times."
- "I can fix this by special-casing one customer."

What the skill should do:

- ask what root cause has been verified
- separate symptom mitigation from real fix
- identify the smallest regression test that proves the behavior
- warn when the fix is becoming a broader rewrite

## 2. Small Feature Scope Check

Example:

- "While adding this field, let's clean up the whole form."
- "This small feature needs a new abstraction."
- "Let's support every future variant now."

What the skill should do:

- keep the first useful version small
- distinguish required cleanup from opportunistic cleanup
- identify what can be deferred safely

## 3. Pull Request Scope Review

Example:

- "This PR fixes a bug, refactors the module, updates tests, and renames helpers."
- "I am not sure whether to split this up."

What the skill should do:

- separate functional changes from cleanup
- call out review risk
- suggest a smaller PR boundary when useful

## 4. Dependency Justification

Example:

- "Let's add a package for this small parser."
- "Let's install a framework for one workflow."
- "Let's add Redis for temporary state."

What the skill should do:

- ask what the dependency is buying
- compare against built-in or local alternatives
- expose maintenance, security, and upgrade cost

## 5. Test Plan Review

Example:

- "These are the tests I plan to add."
- "Do we need integration tests for this?"
- "Can manual testing be enough here?"

What the skill should do:

- tie tests to changed behavior
- flag missing regression coverage
- identify low-value test bulk
- state what remains manually verified

## 6. Architecture Pressure Test

Example:

- "Let's split auth into its own service."
- "Let's move webhook handling into a worker fleet."
- "Let's adopt event-driven architecture."

What the skill should do:

- ask what current pain exists
- check whether modularization inside the current app would solve enough
- expose deploy, monitoring, and compatibility cost

## 7. Infrastructure and Tooling Choices

Example:

- "Let's add Kafka."
- "Let's use eBPF LSM."
- "Let's add Kubernetes now so we are future-proof."

What the skill should do:

- question whether the team needs that operational burden now
- check install-base and compatibility constraints
- suggest a smaller or more reversible step

## 8. Product Feature Sanity Check

Example:

- "Let's add an AI assistant to onboarding."
- "Let's build a recommendation engine."
- "Let's add collaborative editing because power users might want it."

What the skill should do:

- ask what real user pain is being solved
- quantify who benefits and how often
- separate MVP value from feature creep

## 9. AI and Automation Filtering

Example:

- "Let's make the agent auto-fix config problems."
- "Let's make the system fully autonomous."
- "Let's add a smart planner before we even know the workflow."

What the skill should do:

- challenge whether AI is necessary
- distinguish decision support from autonomous action
- recommend a safer validation path first

## 10. Refactor and Rewrite Decisions

Example:

- "Let's rewrite this module in Rust."
- "Let's replace the current UI framework."
- "Let's clean up everything while touching this feature."

What the skill should do:

- ask whether the current system is failing or merely unattractive
- highlight migration cost, regression risk, and opportunity cost
- prefer local simplification over strategic rewrites unless evidence is strong

## 11. Roadmap and Planning Review

Example:

- "Here is the next quarter roadmap."
- "These are the top five features we want."

What the skill should do:

- challenge vague impact claims
- identify items that are outputs rather than outcomes
- expose when "while we're at it" is doubling scope

## 12. Cases Where the Skill Should Agree

The skill is also useful when the right answer is:

- "I looked for a simpler path and do not see one."
- "This is expensive, but the constraints justify it."
- "The cheaper experiment has already been run."

That is a feature, not a failure. The point is discernment, not obstruction.
