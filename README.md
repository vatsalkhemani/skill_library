# Skill Library

A collection of useful [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills I've found online and some I created myself. These are generic, portable prompts that can be dropped into any project.

## What Are Skills?

Claude Code skills are structured prompt files that teach Claude specialized behaviors. Each skill is a self-contained `.md` file with frontmatter metadata and detailed instructions, examples, and rules. When installed in a project's `.claude/skills/` directory, they become available as slash commands (e.g., `/linkedin-writer`).

## Available Skills

### Content Creation

| Skill | Trigger | Description |
|---|---|---|
| [linkedin-writer](.claude/skills/linkedin-writer/SKILL.md) | `/linkedin-writer [topic]` | Drafts LinkedIn posts in a builder-PM voice. Covers voice guidelines, anti-patterns, content pillars, structure shapes, LinkedIn-native formatting, and gold standard examples. |

### Product Management

| Skill | Trigger | Description |
|---|---|---|
| [problem-framer](.claude/skills/problem-framer/SKILL.md) | `/problem-framer` | Decompose vague problems into structured problem statements. Encodes Problem Definition Canvas, 5 Whys, JTBD, opportunity sizing, constraint mapping, and ICE/RICE prioritization. |
| [discovery](.claude/skills/discovery/SKILL.md) | `/discovery` | Synthesize user research, analyze interview data, run discovery sprints, evaluate evidence quality, and build research-backed feature hypotheses. |
| [spec-writer](.claude/skills/spec-writer/SKILL.md) | `/spec-writer` | Write zero-question product specs, feature specs, API contracts, and agent task specs. Encodes outcome-first methodology, acceptance criteria taxonomy, and ambiguity resolution. |
| [narrative-builder](.claude/skills/narrative-builder/SKILL.md) | `/narrative-builder` | Build product positioning, strategy narratives, stakeholder pitches, and launch stories. Encodes April Dunford positioning, Why Now analysis, and objection anticipation. |
| [competitive-analysis](.claude/skills/competitive-analysis/SKILL.md) | `/competitive-analysis` | Perform competitive analysis, moat evaluation, market entry assessment, and positioning using 7 Powers, Aggregation Theory, Christensen Disruption, and Wardley Mapping. |
| [metric-design](.claude/skills/metric-design/SKILL.md) | `/metric-design` | Design metric frameworks, North Star metrics, metric decomposition trees, A/B experiments, retention cohort analysis, and Goodhart's Law countermeasures. |

### Marketing & GTM

| Skill | Trigger | Description | Source |
|---|---|---|---|
| [marketing-strategist](.claude/skills/marketing-strategist/SKILL.md) | `/marketing-strategist` | 139 proven SaaS marketing ideas organized by stage, budget, timeline, and use case. Covers content/SEO, paid ads, partnerships, product-led growth, and more. | [syntax-syndicate/marketing-skills](https://github.com/syntax-syndicate/marketing-skills) |
| [gtm-planner](.claude/skills/gtm-planner/SKILL.md) | `/gtm-planner` | Full go-to-market playbook: ICP definition, April Dunford positioning, competitive battlecards, tiered launch planning, sales enablement, and international expansion. | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) |

### Thinking & Learning

| Skill | Trigger | Description | Source |
|---|---|---|---|
| [deep-thinker](.claude/skills/deep-thinker/SKILL.md) | `/deep-thinker` | First-principles reasoning framework. Break complex problems into fundamental truths by questioning assumptions and rebuilding from irreducible components. Includes mental traps, 5 Whys, and verification checklists. | [tjboudreaux/cc-thinking-skills](https://github.com/tjboudreaux/cc-thinking-skills) |
| [deep-learner](.claude/skills/deep-learner/SKILL.md) | `/deep-learner [orient]` | Interactive learning exercises during AI-assisted coding. Offers prediction/observation/reflection, generation/comparison, trace-the-path, debug-this, and teach-it-back exercises with fading scaffolding. | [DrCatHicks/learning-opportunities](https://github.com/DrCatHicks/learning-opportunities) |

## Usage

### Option 1: Copy a skill into your project

```bash
# From within your target project
mkdir -p .claude/skills/deep-thinker
cp <path-to-this-repo>/.claude/skills/deep-thinker/SKILL.md .claude/skills/deep-thinker/SKILL.md
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
    competitive-analysis/
      SKILL.md
    deep-learner/
      SKILL.md
    deep-thinker/
      SKILL.md
    discovery/
      SKILL.md
    gtm-planner/
      SKILL.md
    linkedin-writer/
      SKILL.md
    marketing-strategist/
      SKILL.md
    metric-design/
      SKILL.md
    narrative-builder/
      SKILL.md
    problem-framer/
      SKILL.md
    spec-writer/
      SKILL.md
CLAUDE.md
README.md
```
