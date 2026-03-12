# Skill Library

A collection of useful [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills I've found online and some I created myself. These are generic, portable prompts that can be dropped into any project.

## Skills

### Product Thinking
- [product-thinker](.claude/skills/product-thinker/SKILL.md)
- [problem-framer](.claude/skills/problem-framer/SKILL.md)
- [discovery](.claude/skills/discovery/SKILL.md)
- [spec-writer](.claude/skills/spec-writer/SKILL.md)
- [competitive-analysis](.claude/skills/competitive-analysis/SKILL.md)
- [metric-design](.claude/skills/metric-design/SKILL.md)
- [product-strategist](.claude/skills/product-strategist/SKILL.md)
- [agile-owner](.claude/skills/agile-owner/SKILL.md)
- [pricing-strategist](.claude/skills/pricing-strategist/SKILL.md)

### Design
- [frontend-designer](.claude/skills/frontend-designer/SKILL.md)
- [ux-researcher](.claude/skills/ux-researcher/SKILL.md)

### Marketing & GTM
- [marketing-strategist](.claude/skills/marketing-strategist/SKILL.md)
- [gtm-planner](.claude/skills/gtm-planner/SKILL.md)
- [narrative-builder](.claude/skills/narrative-builder/SKILL.md)

### Communication & Storytelling
- [storyteller](.claude/skills/storyteller/SKILL.md)
- [linkedin-writer](.claude/skills/linkedin-writer/SKILL.md)

### Thinking & Learning
- [deep-thinker](.claude/skills/deep-thinker/SKILL.md)
- [deep-learner](.claude/skills/deep-learner/SKILL.md)

## Usage

Copy a skill into your project:
```bash
mkdir -p .claude/skills/spec-writer
cp <path-to-this-repo>/.claude/skills/spec-writer/SKILL.md .claude/skills/spec-writer/SKILL.md
```

Or add this repo as a secondary working directory in Claude Code settings.

## Adding a New Skill

1. Create `.claude/skills/<skill-name>/SKILL.md` with frontmatter:
   ```markdown
   ---
   name: skill-name
   description: When to trigger this skill.
   ---
   ```
2. Update `CLAUDE.md`.
