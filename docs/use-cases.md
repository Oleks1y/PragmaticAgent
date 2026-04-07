# Use Cases

`PragmaticAgent` is most useful when the plan sounds impressive but may not yet be justified.

## 1. Architecture Pressure Test

Example:

- "Let's split auth into its own service."
- "Let's move webhook handling into a worker fleet."
- "Let's adopt event-driven architecture."

What the skill should do:

- ask what current pain exists
- check whether modularization inside the current app would solve enough
- expose deploy, monitoring, and compatibility cost

## 2. Infrastructure and Tooling Choices

Example:

- "Let's add Kafka."
- "Let's use eBPF LSM."
- "Let's add Kubernetes now so we are future-proof."

What the skill should do:

- question whether the team needs that operational burden now
- check install-base and compatibility constraints
- suggest a smaller or more reversible step

## 3. Product Feature Sanity Check

Example:

- "Let's add an AI assistant to onboarding."
- "Let's build a recommendation engine."
- "Let's add collaborative editing because power users might want it."

What the skill should do:

- ask what real user pain is being solved
- quantify who benefits and how often
- separate MVP value from feature creep

## 4. AI and Automation Filtering

Example:

- "Let's make the agent auto-fix config problems."
- "Let's make the system fully autonomous."
- "Let's add a smart planner before we even know the workflow."

What the skill should do:

- challenge whether AI is necessary
- distinguish decision support from autonomous action
- recommend a safer validation path first

## 5. Refactor and Rewrite Decisions

Example:

- "Let's rewrite this module in Rust."
- "Let's replace the current UI framework."
- "Let's clean up everything while touching this feature."

What the skill should do:

- ask whether the current system is failing or merely unattractive
- highlight migration cost, regression risk, and opportunity cost
- prefer local simplification over strategic rewrites unless evidence is strong

## 6. Roadmap and Planning Review

Example:

- "Here is the next quarter roadmap."
- "These are the top five features we want."

What the skill should do:

- challenge vague impact claims
- identify items that are outputs rather than outcomes
- expose when "while we're at it" is doubling scope

## 7. Cases Where the Skill Should Agree

The skill is also useful when the right answer is:

- "I looked for a simpler path and do not see one."
- "This is expensive, but the constraints justify it."
- "The cheaper experiment has already been run."

That is a feature, not a failure. The point is discernment, not obstruction.

