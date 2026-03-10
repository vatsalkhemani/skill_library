# Skill Library

A collection of reusable Claude Code skills for personal productivity and content creation.

## Repository Structure

```
.claude/
  skills/
    <skill-name>/
      SKILL.md        # The skill definition (frontmatter + prompt)
README.md
CLAUDE.md              # This file
```

## Skill Format

Each skill lives in `.claude/skills/<skill-name>/SKILL.md` and follows this structure:

```markdown
---
name: skill-name
description: When and how to trigger this skill.
argument-hint: [optional hint for arguments]
---

<skill prompt content>
```

- **name**: kebab-case identifier (matches the folder name)
- **description**: Short sentence explaining when Claude should use the skill
- **argument-hint**: Optional hint shown to the user for what arguments to pass

## Conventions

- Skill folder names use kebab-case: `linkedin-writer`, not `LinkedIn_post`
- One SKILL.md per skill folder
- Skills should be self-contained — all instructions, examples, and rules in a single file
- Do not add files outside `.claude/skills/` unless they are repo-level docs (README, CLAUDE.md, LICENSE)

## Available Skills

| Skill | Description |
|---|---|
| `linkedin-writer` | Draft LinkedIn posts in the owner's builder-PM voice |
| `problem-framer` | Decompose vague problems into structured problem statements with 5 Whys, JTBD, opportunity sizing, and ICE/RICE prioritization |
| `discovery` | Synthesize user research, analyze interviews, run discovery sprints, and build research-backed hypotheses |
| `spec-writer` | Write zero-question product specs, feature specs, API contracts, and agent task specs |
| `narrative-builder` | Build product positioning, strategy narratives, stakeholder pitches, and launch stories |
| `competitive-analysis` | Perform competitive analysis, moat evaluation, and positioning using 7 Powers, Aggregation Theory, and Wardley Mapping |
| `metric-design` | Design metric frameworks, North Star metrics, A/B experiments, and retention cohort analysis |
