# Skill Library

A personal collection of reusable [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills — generic, portable prompts that can be dropped into any project.

## What Are Skills?

Claude Code skills are structured prompt files that teach Claude specialized behaviors. Each skill is a self-contained `.md` file with frontmatter metadata and detailed instructions, examples, and rules. When installed in a project's `.claude/skills/` directory, they become available as slash commands (e.g., `/linkedin-post`).

## Available Skills

| Skill | Trigger | Description |
|---|---|---|
| **linkedin-post** | `/linkedin-post [topic]` | Drafts LinkedIn posts in a builder-PM voice. Covers voice guidelines, anti-patterns, content pillars, structure shapes, LinkedIn-native formatting, and gold standard examples. |

## Usage

### Option 1: Copy a skill into your project

```bash
# From within your target project
mkdir -p .claude/skills/linkedin-post
cp <path-to-this-repo>/.claude/skills/linkedin-post/SKILL.md .claude/skills/linkedin-post/SKILL.md
```

### Option 2: Add this repo as a secondary working directory

In your Claude Code settings, add this repo as an additional working directory. Claude will pick up all skills automatically.

## Adding a New Skill

1. Create a folder under `.claude/skills/` with a kebab-case name:
   ```
   .claude/skills/my-new-skill/
   ```
2. Add a `SKILL.md` file with frontmatter:
   ```markdown
   ---
   name: my-new-skill
   description: Short description of when to trigger this skill.
   argument-hint: [optional arguments]
   ---

   <Your detailed skill prompt here>
   ```
3. Update the table in this README and in `CLAUDE.md`.

## Structure

```
.claude/
  skills/
    linkedin-post/
      SKILL.md
CLAUDE.md
README.md
```
