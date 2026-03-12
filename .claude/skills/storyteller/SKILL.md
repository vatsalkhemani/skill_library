---
name: storyteller
description: "Craft compelling stories and narratives for any context — presentations, pitches, blog posts, product launches, team communication, or public speaking. Produces a Narrative Draft with structural choices made explicit. Use when the user needs to make an idea resonate, persuade an audience, explain something complex simply, or turn facts into a narrative that moves people. Trigger keywords: story, storytelling, pitch, presentation, communicate, persuade, narrative, explain, make this compelling."
argument-hint: "idea, topic, or context to tell a story about"
---

## Purpose

Produce a **Narrative Draft** — a story so well-structured that the hook earns attention, the tension sustains it, the insight rewards it, and the close makes it stick. The output is not a generic "once upon a time" wrapper around the user's content — it is a deliberately architected narrative where every element (hook type, framework choice, audience adaptation, specificity level, emotional anchor placement) traces to a structural decision. The kind of storytelling that makes audiences lean forward, remember the key point a week later, and take the action the story was designed to drive.

## When to Use / When NOT to Use

**Use this skill when:**
- Crafting a pitch or presentation narrative
- Making a complex idea simple and memorable
- Writing a compelling blog post, memo, or announcement
- Preparing for a talk, interview, or public speaking event
- Turning dry data or product updates into engaging communication
- Persuading stakeholders, investors, or team members
- Building a product launch story or company narrative
- Any time the user says: "make this compelling", "help me explain", "how do I pitch this"

**Do NOT use this skill when:**
- Writing product specifications (→ spec-writer — precision, not narrative)
- Writing technical documentation, API docs, or runbooks (those need clarity, not story arc)
- Legal or compliance content requiring precise, non-narrative language
- The user wants bullet points or a quick summary, not a narrative
- Writing LinkedIn posts (→ linkedin-writer — platform-specific voice and format)

**Anti-inputs (what this skill does NOT handle):**
- Product positioning strategy (→ narrative-builder — that's strategic positioning with evidence tiers, this is storytelling craft)
- Competitive narratives (→ competitive-analysis for the intelligence, then this skill to tell the story)
- User research synthesis (→ discovery — that's evidence, this shapes evidence into story)
- Metric design or data analysis (→ metric-design — this skill can make data interesting, but doesn't design the metrics)

---

## Format Rules

These rules govern every narrative output. They prevent the most common storytelling failures: weak openings, no tension, abstract language, buried insights, and forgettable closes.

### Rule 1: The One-Sentence Spine Comes First

Before building any narrative, compress the entire story into one sentence:

**[Character] wants [goal] but faces [obstacle], so they [action], which results in [outcome].**

If you can't fill in this sentence, the story isn't ready. Ask the user for more material. Do not begin drafting without a spine.

**Why this matters:** Every detail in the narrative either supports this spine or dilutes it. The spine is the test: "Does this paragraph advance the story?" Without it, narratives wander.

### Rule 2: Framework Selection is a Decision, Not a Default

Explicitly choose and name which narrative framework you're using and why. Never default to Three-Act Structure because it's familiar.

**Why this matters:** The wrong framework produces the wrong shape. An executive memo using Hero's Journey wastes their time. A product launch story using SCR buries the emotional hook. Framework selection is the single highest-leverage decision in storytelling.

### Rule 3: The Hook Must Create a Gap

The opening must create a gap — between what the audience knows and what they're about to learn, or between what they expect and what actually happened. If the first two sentences don't create a gap, rewrite them.

**Why this matters:** 80% of audiences decide to keep reading or listening based on the first 10 seconds. A hook that starts with background, context, or definitions has already lost.

### Rule 4: Specificity Over Abstraction, Always

Replace every abstract claim with a concrete detail, number, or scene. "We improved performance" → "Load time dropped from 3.2s to 400ms." "Many users were unhappy" → "47 support tickets in one week, all saying the same thing."

**Why this matters:** Specifics create credibility and imagery. Abstractions create nothing. An audience remembers "14 missed calls at 2 AM" — they don't remember "significant operational challenges."

### Rule 5: Tension Must Escalate Before It Resolves

Introduce tension early, escalate it at least once, resolve it late. Never resolve tension in the same paragraph you introduce it.

**Why this matters:** Most weak narratives resolve tension too quickly or never escalate it. Without escalation, there's no reason for the audience to keep listening. The turning point must feel earned.

### Rule 6: The Close Must Land, Not Trail Off

The last line is the first thing they'll remember. It must be one of: callback, one-liner, forward look, genuine question, or specific challenge. Never end with a summary, "any questions?", or a generic call to action.

**Why this matters:** A weak close retroactively weakens the entire narrative. The audience's last impression becomes their overall impression.

### Rule 7: Audience Determines Everything

The same material requires completely different treatment for executives vs. engineers vs. customers vs. the public. Framework, length, specificity level, hook type, and close type all adapt to audience.

**Why this matters:** A narrative crafted for "everyone" resonates with no one. Audience-blind storytelling is the most common cause of "the content was good but it didn't land."

---

## Narrative Strength Scoring

After drafting, score the narrative on these five dimensions. Each is 0-3:

| Dimension | 0 (Broken) | 1 (Weak) | 2 (Solid) | 3 (Exceptional) |
|---|---|---|---|---|
| **Hook** | Starts with background/context | Creates mild interest | Creates a clear gap | Gap is irresistible — audience MUST know what's next |
| **Tension** | No tension present | Tension introduced but resolved immediately | Tension introduced and escalated once | Tension escalates multiple times, turning point feels earned |
| **Specificity** | All abstract claims | Mix of abstract and specific | Mostly specific details and numbers | Every claim grounded in vivid, concrete detail |
| **Insight** | No clear takeaway | Obvious/expected takeaway | Non-obvious insight the audience hadn't considered | Insight reframes how the audience thinks about the topic |
| **Close** | Trails off or summarizes | Adequate ending | Strong close using one of the five patterns | Close is quotable and the audience will repeat it |

**Score thresholds:**
- **12-15**: Ready to present. The narrative works.
- **9-11**: Functional but needs polish on weak dimensions. Flag which ones.
- **0-8**: Structural problems. Don't present — rework.

---

## Output Template (Mandatory Structure)

Every Narrative Draft MUST include these elements. The narrative itself is the primary output; the structural notes are the scaffolding that makes it reviewable and adjustable.

```markdown
# Narrative Draft: [Title or topic]

> **Audience:** [who this is for]
> **Framework:** [which framework and why]
> **Use case:** [presentation / blog / memo / pitch / talk / launch / alignment]
> **Target length:** [word count or time]
> **Narrative Strength Score:** [X/15]

---

## Spine

[The one-sentence story: Character wants goal but faces obstacle, so they action, resulting in outcome.]

---

## The Narrative

[The actual draft — ready to deliver. No structural annotations inline. Clean, readable, presentable.]

---

## Structural Notes (For the Author)

**Hook type used:** [Surprising fact / Provocative question / Vivid scene / Bold claim / Tension / In medias res]
**Tension mechanism:** [Uncertainty / Stakes / Contradiction / Time pressure / Conflict]
**Emotional anchor:** [Where it is and what emotion it targets]
**Insight placement:** [Where the non-obvious idea lands]
**Close type:** [Callback / One-liner / Forward look / Question / Challenge]

**Proposed adjustments:** [What the author might want to change — tone, length, audience, angle]

---

## Dimension Scores

| Dimension | Score | Note |
|---|---|---|
| Hook | [0-3] | [brief note] |
| Tension | [0-3] | [brief note] |
| Specificity | [0-3] | [brief note] |
| Insight | [0-3] | [brief note] |
| Close | [0-3] | [brief note] |
| **Total** | **[X/15]** | |
```

---

## Step 0: Story Type Routing

Before selecting a framework, identify the story type. This determines which framework fits, what depth is needed, and how to adapt for audience.

| Story type | Example | Best framework | Key requirement | Target length |
|---|---|---|---|---|
| **Executive pitch** | "Here's what we should do and why" | SCR (Situation-Complication-Resolution) | Lead with resolution. Under 2 min verbal, under 1 page written | 200-400 words |
| **Product launch** | "Here's what we built and why it matters" | Contrast Pattern or Three-Act | The hero is the user, not the product | 300-600 words |
| **Lessons learned** | "Here's what went wrong and what we learned" | Three-Act (Build Log variant) | Specific failure, non-obvious lesson | 400-700 words |
| **Vision / strategy** | "Here's where the world is going and why we should act" | Hero's Journey or Contrast Pattern | "Why now" must be compelling | 500-800 words |
| **Team alignment** | "Here's where we are and what we're doing next" | Three-Act (direct variant) | Honesty, specificity, clear asks | 300-500 words |
| **Data → story** | "Here's what the data says and why it matters" | Three-Act (insight variant) | Start with the most surprising data point | 200-400 words |
| **Blog / social** | "Here's an idea worth spreading" | Pixar Formula (for testing) → any framework for execution | One idea per piece. Hook is everything | 150-500 words |
| **Investor / board** | "Here's the market narrative and our position in it" | Hero's Journey | Market insight first, company second | 500-1000 words |
| **Talk / keynote** | "Here's a journey I'll take you on" | Hero's Journey or Contrast Pattern | In medias res hook. Callback close | 1000-2000 words |

---

## The Storytelling Frameworks

### Framework 1: Three-Act Structure

The foundation. Works for most narrative types.

**Act 1: Setup (10-15%)**
- The world as it is. The character. The planted tension.

**Act 2: Confrontation (70-75%)**
- The struggle. Rising stakes. The turning point.

**Act 3: Resolution (10-15%)**
- The new world. The lesson. The call to action.

### Framework 2: Pixar Formula

Six sentences for rapid narrative prototyping:

1. **Once upon a time** there was [context].
2. **Every day**, [status quo].
3. **One day**, [disruption].
4. **Because of that**, [first consequence].
5. **Because of that**, [escalation].
6. **Until finally**, [resolution].

Use this to test narrative movement. If steps 4-5 are flat, the story lacks tension.

### Framework 3: Hero's Journey (Business-Condensed)

For longer narratives: launches, origin stories, transformation pitches.

1. **Ordinary World** → 2. **The Call** → 3. **Resistance** → 4. **The Guide** → 5. **The Threshold** → 6. **Trials** → 7. **Transformation** → 8. **The Return**

### Framework 4: SCR (Situation-Complication-Resolution)

The McKinsey classic. Best for executive communication.

- **Situation**: Uncontroversial current state (1-2 sentences)
- **Complication**: What disrupts it (this is where you earn attention)
- **Resolution**: Your recommended path (this is where you earn trust)

### Framework 5: Contrast Pattern

For persuasive content. Alternate "what is" and "what could be":

```
What is → What could be → What is → What could be → What is → What could be (vivid, final)
```

The gap between reality and possibility creates emotional tension demanding resolution.

---

## The Building Blocks

### 1. Hook Types

| Type | Example | Best for |
|---|---|---|
| **Surprising fact** | "80% of features are used by <5% of users" | Data-driven audiences |
| **Provocative question** | "What if the problem isn't the tech — it's the question?" | Thought leadership |
| **Vivid scene** | "2 AM. Production is down. 14 missed calls." | Empathy-building |
| **Bold claim** | "The best strategy doc is one page long" | Contrarian takes |
| **Tension** | "We had the best model. Users hated it." | Lessons learned |
| **In medias res** | Start in the middle, explain context after | Talks, blog posts |

**Never hook with:** definitions, apologies, context dumps, or "What if I told you..."

### 2. Tension Sources

- **Uncertainty**: Will this work?
- **Stakes**: What if it fails? (Make consequences concrete)
- **Contradiction**: Two truths that can't coexist
- **Time pressure**: A deadline or closing window
- **Conflict**: Between people, ideas, priorities

### 3. Specificity — The Rule of Three Details

When describing a scene, include exactly three specific details. One is sparse. Five is cluttered. Three creates a picture: "2 AM, production was down, and my phone showed 14 missed calls."

| Abstract (weak) | Specific (strong) |
|---|---|
| "We improved performance significantly" | "Load time dropped from 3.2s to 400ms" |
| "Many users were unhappy" | "47 support tickets in one week, all the same" |
| "The team worked hard" | "Three engineers until midnight, six days straight" |

### 4. Emotional Anchor

Every narrative needs one moment the audience *feels*. Create it by:
- **Zooming in**: Big picture → one person, one moment
- **Sensory language**: What did it look/feel/sound like?
- **Vulnerability**: The mistake, the doubt
- **Recognition**: "You've felt this too..."

### 5. The Insight

The payload the audience takes away. Must be:
- **Non-obvious**: Not something they already know
- **Transferable**: They can apply it to their own context
- **Concise**: One sentence
- **Earned**: The story makes it feel inevitable

### 6. Close Types

| Close | Mechanism | Example |
|---|---|---|
| **Callback** | Return to the opening, but audience sees it differently now | Open with "2 AM, production down" → close with "It's 2 AM again. This time, the system caught it before my phone rang" |
| **One-liner** | Distill the narrative into one quotable sentence | "Start with the friction, not the model." |
| **Forward look** | Prediction grounded in the story's logic | "In three years, every dashboard will need a human-vs-agent filter" |
| **Question** | A genuine question they'll keep thinking about | "If half your traffic is AI agents, is a page view still a page view?" |
| **Challenge** | Specific action tied to what they learned | "Pick one automation that's been nagging you. Build it this weekend." |

**Never close with:** summaries, "any questions?", "so yeah", or "let's make it happen."

---

## Audience Adaptation

| Audience | Framework default | Key adaptation | Length |
|---|---|---|---|
| **Executives** | SCR | Lead with resolution. Numbers first. One ask | <1 page / <2 min |
| **Technical teams** | Three-Act (Build Log) | Respect expertise. Code is a valid story element | Medium |
| **Customers** | Contrast Pattern | Their pain first, your solution second. Hero = customer | Medium |
| **Investors / Board** | Hero's Journey | Market narrative first, company second. Metrics as evidence | Long |
| **General public** | Any (Pixar to test) | Hook is everything. One idea per piece. Conversational | Short |

---

## Anti-Patterns — Narrative Failures and Their Mechanisms

| Anti-Pattern | Mechanism of failure | Detection |
|---|---|---|
| Starting with background/history | Audience hasn't earned patience. Attention lost before the story begins | Ask: "Do the first two sentences create a gap?" If no, rewrite |
| Burying the insight | Audience tuned out before the payoff | Check: where does the insight appear? If last 10%, surface earlier |
| Making yourself the hero | Audiences connect with vulnerability, not victory laps | Check: who's the protagonist? If it's you winning, reframe |
| Jargon without earning it | Excludes part of the audience, signals insider-speak over clarity | Test: would a smart non-expert understand every sentence? |
| Telling what to feel | "This was exciting" — if you have to say it, it wasn't | Search for emotion words. Replace each with a scene that creates the emotion |
| Details that don't serve the spine | Every neutral detail dilutes. No detail is free | Test each paragraph: "Does this advance the spine?" If no, cut |
| Ending with "so yeah" | Tells the audience the story didn't matter | Check the last sentence: is it one of the five close types? |
| Using stories as decoration | Audience can tell when the conclusion was decided before the story | Check: does the story genuinely lead to the insight, or is it bolted on? |
| Same framework every time | Formulaic = forgettable | Track: what framework did you use last time? Use a different one |

---

## Process

When the user provides material to turn into a story:

1. **Step 0: Route** — What story type is this? (Executive pitch / launch / lessons learned / vision / alignment / data / blog / investor / talk) This determines framework, length, and audience adaptation

2. **Build the spine** — Compress to one sentence. If there are multiple stories embedded, flag them and ask which to focus on

3. **Choose audience** — Who is this for? Lock in the audience adaptation before writing a word

4. **Select framework** — Name which and why. Don't default to Three-Act

5. **Find the hook** — What's the most surprising, vivid, or tension-filled entry point? Write 2-3 hook options, pick the strongest

6. **Draft the narrative** — Follow the framework. Apply the building blocks: specificity, tension escalation, emotional anchor, earned insight, intentional close

7. **Score it** — Rate each of the five dimensions (Hook, Tension, Specificity, Insight, Close) on 0-3. Total must be 9+ to present

8. **Present with structural notes** — Show the narrative, then the scaffolding: spine, framework, hook type, tension mechanism, close type. Flag proposed adjustments

After presenting, offer: "Want me to adjust the angle, audience, framework, length, or emotional tone?"
