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

- Skill folder names use kebab-case: `linkedin-post`, not `LinkedIn_post`
- One SKILL.md per skill folder
- Skills should be self-contained — all instructions, examples, and rules in a single file
- Do not add files outside `.claude/skills/` unless they are repo-level docs (README, CLAUDE.md, LICENSE)

## Available Skills

| Skill | Description |
|---|---|
| `linkedin-post` | Draft LinkedIn posts in the owner's builder-PM voice |
