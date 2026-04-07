# Install

`PragmaticAgent` is intentionally simple to install because the asset is instructional, not executable.

## Option 1: Keep the Repository and Reference It

Clone the repository locally and keep it as the source of truth.

This is the best option if you want:

- the full docs set
- easy updates
- a reusable GitHub home for sharing

Then tell Codex to follow [`.codex/INSTALL.md`](../.codex/INSTALL.md).

## Option 2: Copy the Skill Into Your Codex Skills Directory

Create a local skill folder:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor
```

Copy the main skill file:

```bash
cp /path/to/PragmaticAgent/SKILL.md ~/.codex/skills/pragmatic-advisor/SKILL.md
```

Optional docs copy:

```bash
mkdir -p ~/.codex/skills/pragmatic-advisor/docs
cp -R /path/to/PragmaticAgent/docs/* ~/.codex/skills/pragmatic-advisor/docs/
```

## Verification

After installation, invoke it directly in Codex:

```text
Use skill `pragmatic-advisor`.

I want to add a new queue, Redis, and a worker service.
Pressure-test this plan before we implement anything.
```

If the skill is being used correctly, the response should:

- challenge the actual problem statement
- identify hidden assumptions
- call out operational and maintenance cost
- suggest a smaller validation path if one exists

## Updating

If you installed by copying files, update by replacing `SKILL.md` and any docs you want to keep locally.

If you kept the repository as the source of truth, pull the latest changes and refresh your local skill copy when needed.

