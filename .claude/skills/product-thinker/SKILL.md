---
name: product-thinker
description: "The foundational product thinking skill. Use when making product decisions, evaluating trade-offs, thinking through user problems, assessing ideas, or when the user needs a product-minded thought partner. This is the 'how to think' skill, not the 'how to execute' skill — it sits above spec-writing, discovery, metrics, and strategy. Produces a Product Decision Brief. Trigger keywords: should we build this, product decision, trade-off, user problem, prioritize, product sense, what would you do, think through this, evaluate this idea."
argument-hint: "product question, decision, or idea to think through"
---

## Purpose

Produce a **Product Decision Brief** — a structured thinking artifact that makes product reasoning visible, trade-offs explicit, and recommendations defensible. The output is not a gut-feel opinion or a pros/cons list — it is a calibrated assessment that traces from user problem through frameworks to a specific recommendation with named assumptions and reversal conditions. The kind of product thinking that looks like "good instinct" but is actually rigorous analysis made legible.

## When to Use / When NOT to Use

**Use this skill when:**
- Evaluating whether to build something ("should we build this?")
- Making trade-off decisions (scope, timeline, quality, audience)
- Thinking through a user problem from first principles
- Assessing a product idea, feature request, or strategy
- Deciding between competing priorities or approaches
- When the user says: "what do you think about this idea?", "help me think through this", "should we launch?"

**Do NOT use this skill when:**
- Writing a spec (→ spec-writer — that's execution, this is decision-making)
- Conducting user research (→ discovery — that's evidence gathering, this consumes evidence)
- Designing metrics (→ metric-design — that's measurement design, this is outcome framing)
- Building competitive analysis (→ competitive-analysis — that's market structure, this is product judgment)
- Writing positioning or narratives (→ narrative-builder or storyteller)

**Anti-inputs (what this skill does NOT handle):**
- Feature specification details (→ spec-writer produces the zero-question spec)
- Statistical experiment design (→ metric-design handles statistical validity)
- Competitive moat assessment (→ competitive-analysis with 7 Powers framework)
- Organizational strategy or team structure (→ product-strategist)

This skill is the **thinking layer**. It tells you WHICH execution skill to reach for and WHY.

---

## Format Rules

These rules govern every product thinking output. They are not style preferences — they are mechanisms that prevent the most common product thinking failures: ungrounded opinions, invisible trade-offs, and unexamined assumptions.

### Rule 1: Every Recommendation Gets a Rationale Chain

Never state a recommendation without the reasoning chain that produced it. Format:

```
OBSERVATION [what we see] → IMPLICATION [why it matters] → RECOMMENDATION [what to do] → CONFIDENCE [H/M/L + key assumption] → REVERSAL [what would change this recommendation]
```

**Why this matters:** Product opinions without reasoning chains are indistinguishable from guesses. The chain makes thinking auditable, debatable, and improvable. The Reversal condition is what separates conviction from stubbornness.

### Rule 2: Confidence Levels on Every Conclusion

Never present a product conclusion without a confidence tag:

- **H (>70%)** — Based on validated user data, past experiments, or strong analogies from comparable products. Act on it.
- **M (40-70%)** — Based on reasonable inference, industry patterns, or limited direct evidence. Validate before committing significant resources.
- **L (<40%)** — Hypothesis only. Based on first-principles reasoning or intuition. Must be tested before treating as fact.

**Why this matters:** An H-confidence "don't build this" requires different action than an L-confidence one. Without calibration, every recommendation sounds equally certain, which makes all of them equally ignorable.

### Rule 3: Trade-Offs Must Be Named, Not Hidden

Every recommendation trades something away. Name it explicitly:

```
By choosing X, we gain [benefit] but accept [cost].
The alternative (Y) would gain [different benefit] at [different cost].
We recommend X because [specific reason the trade-off favors X in this context].
```

**Why this matters:** Hidden trade-offs are the #1 cause of post-launch "why didn't we think of that?" moments. Visible trade-offs allow the decision-maker to weigh them — which is their job, not ours.

### Rule 4: Assumptions Must Be Surfaced

Every non-trivial conclusion rests on assumptions. Tag them:

- `[Validated]` — confirmed by data, research, or stakeholder decision
- `[Assumed]` — reasonable but unconfirmed. If wrong, conclusion changes
- `[Unknown]` — explicitly unknown. Must be resolved before acting

**Why this matters:** A recommendation built on 3 unvalidated assumptions looks identical to one built on validated data — unless you annotate. The annotations tell the decision-maker where to focus their scrutiny.

### Rule 5: Route to the Right Thinking Level (Step 0)

Different product questions require different thinking depths. Don't apply all frameworks to every question.

**Why this matters:** Using the full Product Thinking Operating System on "should we change the button color?" is overkill. Using a quick heuristic on "should we enter a new market?" is reckless. Step 0 routing prevents both.

### Rule 6: Anti-Inputs Get Redirected, Not Answered

If the user's question is actually a research question, a spec question, or a metrics question masquerading as a product thinking question — redirect to the appropriate skill rather than producing a weaker version of what that skill does well.

**Why this matters:** "Help me think about our activation metrics" sounds like product thinking but is actually metric-design. Answering it here produces surface-level output that misses the statistical rigor of the dedicated skill.

---

## Output Template (Mandatory Structure)

Every Product Decision Brief MUST follow this structure. Scale depth to the question type (see Step 0), but don't skip sections — mark lightweight sections as "N/A — [reason]" rather than omitting them.

```markdown
# Product Decision Brief: [Decision in question form — e.g., "Should we add a free tier?"]

> **Decision type:** [Build/kill/prioritize/launch/pivot — from Step 0]
> **Confidence band:** [Overall H/M/L]
> **Thinking levels applied:** [Problem / Solution / Systems — which are load-bearing]
> **Date:** [YYYY-MM-DD]

---

## Executive Summary

[3 sentences max. A VP reads only this and makes a decision. State the question, the recommendation, and the single strongest reason. No frameworks, no jargon.]

---

## The Question

[Restate the decision precisely. Often the user's original question needs sharpening — "should we build X?" becomes "should we invest [N weeks/people] in X, given that we'd be deprioritizing Y and Z?"]

---

## Problem Assessment (Level 1)

### Who has this problem?
[Specific user segment — not "users"]

### How do they solve it today?
[Current solution, including "doing nothing"]

### What's broken about the current solution?
[Specific failure points]

### Frequency and intensity
[How often? How painful? Daily = product, annual = feature, one-time = service]

### Willingness to switch
[What would they give up? Time, money, learning curve?]

**Problem validity:** [H/M/L — is this a real, painful, frequent problem?]

---

## Solution Assessment (Level 2)

| Dimension | Assessment | Confidence |
|---|---|---|
| **Efficacy** — Does this solve the problem? | [assessment] | [H/M/L] |
| **Usability** — Can the user figure it out? | [assessment] | [H/M/L] |
| **Viability** — Can we build and maintain it? | [assessment] | [H/M/L] |
| **Differentiation** — Why choose this over alternatives? | [assessment] | [H/M/L] |
| **Timing** — Why now? | [assessment] | [H/M/L] |

---

## Systems Assessment (Level 3)

| Question | Answer | Implication |
|---|---|---|
| If this succeeds, what breaks? | [answer] | [what we need to prepare] |
| Who else does this affect? | [answer] | [stakeholders to align] |
| What does this incentivize? | [answer] | [behavior we're creating] |
| What's the maintenance cost? | [answer] | [ongoing investment] |
| What does this prevent later? | [answer] | [path dependencies created] |

---

## Frameworks Applied

[Apply 1-3 frameworks from the toolkit below. Name which and why. Don't apply all five to every question.]

---

## Trade-Off Analysis

**By choosing [recommendation], we gain:**
- [benefit 1]
- [benefit 2]

**We accept:**
- [cost 1]
- [cost 2]

**The alternative ([option B]) would:**
- Gain: [different benefits]
- Cost: [different costs]

**Why this trade-off favors our recommendation:** [specific reason in this context]

---

## Assumption Registry

| # | Assumption | Status | Impact if wrong | Validator |
|---|---|---|---|---|
| 1 | [assumption] | [Validated/Assumed/Unknown] | [what changes] | [who confirms] |
| 2 | [assumption] | [Validated/Assumed/Unknown] | [what changes] | [who confirms] |

---

## Recommendation

**OBSERVATION** [what we see] →
**IMPLICATION** [why it matters] →
**RECOMMENDATION** [what to do — specific, actionable] →
**CONFIDENCE** [H/M/L + the key assumption this rests on] →
**REVERSAL** [what evidence would change this recommendation]

---

## Next Steps

1. [Immediate action + owner]
2. [Validation needed + method + timeline]
3. [Which execution skill to use next: spec-writer / discovery / metric-design]
```

---

## Step 0: Question Type Routing

Before applying any framework, identify the question type. This determines which thinking levels are load-bearing and which frameworks to apply.

| Question type | Example | Load-bearing levels | Frameworks to apply | Depth |
|---|---|---|---|---|
| **Build decision** | "Should we build X?" | All three (Problem → Solution → Systems) | One-Way/Two-Way Door + Opportunity Cost + Solution Quality Test | Full brief |
| **Kill decision** | "Should we kill this failing feature?" | Solution + Systems (problem was already validated or invalidated) | Sunk Cost Check + Reversal Test | Medium brief |
| **Prioritization** | "What should we build next?" | Problem (for each candidate) + comparison | ICE Score + Opportunity Cost | Comparative brief |
| **Launch decision** | "Should we launch now or wait?" | Solution + Systems (is it ready? what breaks?) | One-Way/Two-Way Door + Launch Checklist | Focused brief |
| **Pivot decision** | "The data is mixed — iterate or change direction?" | Problem (was it validated?) + Solution (wrong solution or wrong execution?) | Hypothesis Audit + Sunk Cost Check | Diagnostic brief |
| **Conflict resolution** | "The team disagrees on approach" | Depends on what they disagree about | Name the disagreement precisely → route to the right level | Facilitation brief |
| **Quick gut check** | "What do you think of this idea?" | Problem only (Level 1) — just the Five Questions | Five Questions only | 5-minute brief |

**If the question doesn't fit any type, ask the user to sharpen it.** A vague question produces vague thinking.

---

## The Product Thinking Operating System

### Level 1: Problem Thinking

Before anything else — before solutions, before features, before roadmaps — understand the problem.

**The Five Questions:**

1. **Who has this problem?** Be specific. "Users" is not an answer. "Enterprise security admins managing 50+ seats who onboard new employees monthly" is.

2. **How do they solve it today?** Every problem has a current solution, even if it's "doing nothing" or "using a spreadsheet." The current solution reveals the real bar you must clear.

3. **What's broken about the current solution?** Not "it could be better" — what specifically fails, frustrates, or costs them? If you can't name the pain precisely, you don't understand it yet.

4. **How often do they hit this problem?** Daily pain is a product. Annual pain is a feature. One-time pain is a service. Frequency determines willingness to adopt.

5. **What would they give up to solve it?** Time, money, switching cost, learning curve. This reveals true intensity. If they wouldn't switch from a spreadsheet, the problem isn't painful enough.

**Rule: If you can't answer all five, you're not ready to discuss solutions. [Locked]**

### Level 2: Solution Thinking

**The Solution Quality Test:**

| Dimension | Question | Red flag |
|---|---|---|
| **Efficacy** | Does this actually solve the problem? | "It addresses the symptoms but not the root cause" |
| **Usability** | Can the target user figure this out without help? | "It's powerful but has a learning curve" |
| **Viability** | Can we build and maintain this? | "It requires a new data pipeline, three integrations, and a policy change" |
| **Differentiation** | Why would someone choose this over alternatives? | "It's like X but slightly better" (not enough to switch) |
| **Timing** | Why now? What changed? | "We've wanted to do this for a while" (no urgency = no priority) |

A strong solution scores well on all five. Most ideas score well on 1-2 and fail on the rest.

### Level 3: Systems Thinking

Every product decision has second-order effects. Think in systems, not features.

- **If this succeeds, what breaks?** A 10x increase in signups breaks onboarding. A viral feature breaks moderation.
- **Who else does this affect?** The feature for power users that confuses new users.
- **What does this incentivize?** Metrics that reward quantity reduce quality. Free tiers that are too generous kill conversion.
- **What's the maintenance cost?** Building is 20% of the cost. Maintaining is 80%.
- **What does this prevent us from doing later?** Architectural choices and public API contracts create path dependencies.

---

## The Decision Frameworks

### Framework 1: One-Way / Two-Way Door

Is this decision reversible?

- **Two-way door** (reversible): Decide fast. Ship it, learn, adjust. Examples: copy changes, UI experiments, pricing page layout.
- **One-way door** (irreversible): Slow down. Gather more data. Examples: pricing model changes, platform migrations, public API contracts.

**Most decisions are two-way doors treated as one-way doors.** This is the #1 cause of slow product teams. [H]

### Framework 2: ICE Score

For ranking a backlog:

- **Impact** (1-10): How much does this move the target metric?
- **Confidence** (1-10): How sure are we? (User research = 8-10, data = 6-8, intuition = 3-5, opinion = 1-3)
- **Ease** (1-10): How easy to build? (1 = months, 10 = a day)

**ICE = Impact x Confidence x Ease.** The value is in the conversation, not the math.

### Framework 3: Opportunity Cost Lens

Every yes is a no to something else.

1. What are we NOT doing if we do this? (Top 3)
2. Is this more valuable than all of those?
3. Is this the cheapest way to learn if it's valuable?

### Framework 4: User Value / Business Value Matrix

| | Low Business Value | High Business Value |
|---|---|---|
| **High User Value** | Build this (find the business model later) | **Build this first** (user love + business impact) |
| **Low User Value** | Don't build | Build carefully (risk of dark patterns) |

### Framework 5: Regret Minimization

For high-stakes decisions: **"In 5 years, will we regret NOT doing this more than we'd regret doing it and failing?"**

---

## Thinking Through Common Product Questions

### "Should we build this feature?"

Run through in order:
1. What problem does this solve? (Level 1 — Five Questions)
2. Does our solution pass the Solution Quality Test? (Level 2)
3. What's the opportunity cost? (Framework 3)
4. Is this a one-way or two-way door? (Framework 1)
5. What breaks if this succeeds? (Level 3)

If it survives all five, it's worth building. Most ideas die at step 1-2.

### "How should we prioritize?"

1. Define the single metric you're optimizing this quarter
2. ICE score each candidate (Framework 2)
3. Apply opportunity cost to the top 5 (Framework 3)
4. Check for one-way doors that need more diligence (Framework 1)
5. Sequence: quick wins first, then big bets

### "Should we launch now or wait?"

- **What do we learn by launching that we can't learn otherwise?** (If "a lot", launch)
- **What's the cost of a bad launch?** (Security, data loss, legal = wait. "Not perfect yet" = launch)
- **Can we launch to a subset?** (Beta, 1% rollout — always prefer incremental exposure)

**Default to launching sooner.** Real user feedback > internal speculation. [H]

### "Kill or iterate?"

1. What was the original hypothesis?
2. Was the hypothesis validated? (Did users have the problem?)
3. If yes — wrong solution or wrong execution?
4. **Sunk cost check**: Knowing what you know now, would you start this today? If no, kill it.

### "The team disagrees"

1. Name the disagreement precisely (goal vs approach vs timing)
2. What evidence would change each person's mind?
3. Who owns this decision? (Accountable person decides)
4. Can we run a test instead of having a debate?
5. Disagree and commit. Revisit at next checkpoint.

---

## The Product Thinker's Mental Models

### Outcomes, Not Outputs

- **Output**: We shipped the notification feature
- **Outcome**: Users who opt in retain 2x better at day 30

If you can't articulate the expected outcome, you don't know why you're building it.

### Jobs to Be Done

Users don't want your feature. They want progress. They "hire" your product to do a job. People don't buy drills — they buy the shelf on the wall, the photo displayed, the feeling of home.

### Thinking in Constraints

Constraints are design inputs, not obstacles.

- **Time**: "We have 2 weeks" → What's the smallest thing that validates the hypothesis?
- **Resources**: "One engineer" → What's simple but high-signal?
- **Technical**: "Legacy system" → What works within current architecture?
- **Market**: "Saturated" → Where is everyone serving poorly?

### The 10x Test

A new solution must be 10x better on some dimension to overcome switching costs. The 10x can be: 10x faster (Google), 10x simpler (Stripe), 10x cheaper (Canva), 10x more accessible (Zoom). If you can't identify the 10x dimension, adoption will struggle regardless of quality.

---

## Anti-Patterns — Signs of Weak Product Thinking

| Pattern | Mechanism of failure | Detection |
|---|---|---|
| Starting with the solution | Build something nobody needs | Ask: "What problem does this solve?" If the answer is vague, you started wrong |
| "Users want X" without evidence | Graveyard of products is full of assumed needs | Ask: "Which specific users? How do you know?" |
| Designing by committee | Committees produce compromises, not products | Count decision-makers. If >1, it's a committee |
| Copying competitors | Always behind, no differentiation | Ask: "Why did THEY build it? Does the same reason apply to OUR users?" |
| Optimizing for edge cases | 80% of effort on 5% of users | Check: what % of users does this affect? |
| Conflating activity with progress | Shipping features ≠ moving metrics | Ask: "What changed for users?" not "What did we ship?" |
| Infinite research mode | Research without a decision deadline = procrastination | Check: is there a decision date? If no, set one |
| Ignoring current solutions | Misunderstanding switching cost | Ask: "How do they solve this today? What would make them switch?" |
| "Business model later" | Works once in a generation | Ask: "Who pays? Why? How much?" Even a hypothesis is better than nothing |
| Building for yourself | You are not your user | Ask: "Have we validated this with anyone who isn't us?" |

---

## Process

When the user brings a product question:

1. **Step 0: Route** — What type of question is this? (Build/kill/prioritize/launch/pivot/conflict/gut check) This determines depth and frameworks
2. **Sharpen the question** — Restate it precisely. "Should we build X?" becomes "Should we invest N weeks in X, deprioritizing Y and Z?"
3. **Apply the right level** — Problem thinking first, then solution, then systems. Don't skip levels
4. **Choose 1-3 frameworks** — Pick the ones that are load-bearing for this question type. Don't over-framework
5. **Surface trade-offs explicitly** — Name what you're trading away. Visible trade-offs > hidden trade-offs
6. **Tag confidence and assumptions** — Every conclusion gets H/M/L. Every assumption gets Validated/Assumed/Unknown
7. **State the recommendation with a reversal condition** — "I'd recommend X. I'd change my mind if we learn Y."
8. **Point to the next skill** — "Now take this to spec-writer" or "Validate this assumption with discovery first"

Present thinking transparently. Show reasoning, not just conclusions. Invite the user to challenge assumptions.
