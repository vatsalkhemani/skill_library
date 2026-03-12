---
name: frontend-designer
description: "Design and build beautiful, modern, interactive web UIs. Use when creating landing pages, dashboards, web apps, components, or any frontend work where visual quality matters. Produces a UI Design Brief + production code. Encodes visual hierarchy, typography systems, color architecture, spatial grids, component patterns, animation principles, responsive strategy, and page-type design systems. Trigger keywords: design, beautiful, UI, landing page, dashboard, frontend, make it look good, polish, redesign, modern UI."
argument-hint: "page or component to design"
---

## Purpose

Produce a **UI Design Brief + Production Code** — an implementation so intentional that every visual decision can be traced to a purpose (guide attention, reduce cognitive load, communicate hierarchy, or create delight). The output is not a generic template with swapped colors — it is a designed system: consistent spacing, calibrated typography, structured color, purposeful motion, and responsive behavior. The kind of UI work that looks "obviously right" but requires dozens of deliberate decisions to achieve.

## When to Use / When NOT to Use

**Use this skill when:**
- Building a new page, layout, or component where visual quality matters
- Creating landing pages, marketing pages, or product pages
- Designing dashboards, admin panels, or data-heavy interfaces
- Improving the visual quality of existing UI ("make it look good", "polish this")
- Building a design system or component library
- The user shows you a screenshot or wireframe and wants it implemented beautifully

**Do NOT use this skill when:**
- Pure backend/API work with no UI component
- Performance optimization without visual changes (that's engineering)
- Accessibility audits only (complement with a dedicated a11y review — this skill enforces WCAG AA as a baseline, not as a sole focus)
- The user wants a quick unstyled prototype to test logic (use plain HTML or a UI framework directly)
- Content writing or copywriting (→ storyteller skill for narrative, linkedin-writer for social)

**Anti-inputs (what this skill does NOT handle):**
- UX research or user testing (→ ux-researcher skill)
- Product strategy or feature decisions (→ product-thinker skill)
- Brand identity or logo design (this skill implements an existing brand, it doesn't create one)
- Motion design for video/animation production (this is UI motion, not motion graphics)

---

## Format Rules

These rules govern every design output. They are not aesthetic preferences — they are quality enforcement mechanisms derived from how design actually fails in production.

### Rule 1: Every Visual Decision Gets a Rationale

Never make a design choice without being able to answer "why." Color, spacing, typography, layout, motion — each carries a brief inline rationale on first use. Not "I chose blue" but "Primary action uses `blue-600` — high contrast against the neutral canvas, consistent with the brand's trust signal, passes WCAG AA at 4.7:1."

**Why this matters:** Design without rationale is decoration. Rationale makes designs defensible in review, consistent across iterations, and debuggable when something "feels off."

### Rule 2: Design Token Architecture is Mandatory

Never use hardcoded values (`#3b82f6`, `16px`, `8px`). Every value traces to a design token:
- **Primitives** → `--color-blue-600`, `--space-4`, `--text-base`
- **Semantic** → `--color-primary`, `--space-section`, `--text-body`
- **Component** → `--button-bg`, `--card-padding`, `--nav-height`

Tailwind classes count as tokens. Raw hex/px values in CSS do not.

**Why this matters:** Hardcoded values create invisible inconsistency. Two blues that are 2% different look like a mistake. Tokens enforce consistency at the system level and make dark mode, theming, and responsive adjustments trivial.

### Rule 3: The Squint Test is a Gate, Not a Suggestion

Before presenting any design, apply the squint test: blur or squint at the screen. If the primary element isn't immediately obvious, the hierarchy is broken. Fix it before adding anything else.

**Why this matters:** Users don't read UIs — they scan. If hierarchy fails the squint test, no amount of polish fixes the core problem. This is the single most predictive test of whether a UI "works."

### Rule 4: Design System Before Components

Before coding any component, establish the four foundations:
1. **Type scale** (sizes, weights, line heights, letter spacing)
2. **Color system** (neutral scale, primary, semantic colors, contrast ratios)
3. **Spacing grid** (base unit, scale, section rhythm)
4. **Elevation strategy** (borders OR shadows OR surface color — pick ONE, not all three)

Components built without these foundations will be internally inconsistent.

**Why this matters:** A button without a type scale is a guess. A card without a spacing grid is eyeballed. Design systems eliminate eyeballing and produce outputs that feel "inevitably right."

### Rule 5: State Coverage is Non-Negotiable

Every interactive element must have: **default → hover → active → focus → disabled**. Every data-dependent view must have: **loading → empty → populated → error**. Missing states are bugs, not TODOs.

**Why this matters:** An interface without loading states feels broken. A button without a focus state fails accessibility. State coverage is what separates "prototype" from "production."

### Rule 6: Mobile-First is a Build Order, Not a Philosophy

Write base styles for mobile. Layer desktop enhancements with `min-width` breakpoints. Test at 320px — if it works there, it works everywhere.

**Why this matters:** Mobile-first prevents the common failure of building a desktop layout and then trying to "shrink" it. Subtraction is harder than addition.

### Rule 7: Animation Serves Communication, Not Decoration

Every animation must answer: "What information does this motion communicate?" If the answer is "none, it looks cool," remove it. Valid purposes: spatial relationship (where something came from), state change (something updated), attention direction (look here), feedback (your action registered).

**Why this matters:** Gratuitous animation creates motion sickness risk, degrades performance, and trains users to ignore motion — which means purposeful motion stops working too.

---

## Design Confidence Levels

Design decisions carry different levels of certainty. Annotate decisions that the user might want to adjust:

- **Locked** — Driven by constraints (WCAG contrast, touch target minimums, viewport math). Not negotiable.
- **Recommended** — Best practice with strong evidence. The user can override with a reason.
- **Proposed** — Opinionated choice (color temperature, border radius personality, animation timing). Flag these so the user knows they can adjust.

---

## Output Template (Mandatory Structure)

Every UI implementation MUST include a **UI Design Brief** (inline or as a preamble) before the code. The brief makes design decisions visible and reviewable. The code is the primary deliverable; the brief is the scaffolding.

```markdown
# UI Design Brief: [Page or component name]

> **User:** [who this is for]
> **Primary action:** [the ONE thing the user should do]
> **Mood:** [trust / energy / calm / playful / authority / neutral]
> **Stack:** [React + Tailwind / vanilla / Vue / etc.]
> **Device:** [mobile-first / desktop-primary / responsive-all]

---

## Design Foundations

**Typography:** [font(s), scale ratio, body size]
**Color:** [primary, neutral scale, accent — with rationale]
**Spacing:** [base unit, key spacing tokens]
**Elevation:** [borders / shadows / surface shifts — which and why]

---

## Key Design Decisions

| Decision | Choice | Rationale | Confidence |
|---|---|---|---|
| [e.g., Layout direction] | [e.g., Left sidebar + content] | [e.g., Dashboard convention, users scan nav first] | [Locked/Recommended/Proposed] |
| [e.g., Border radius] | [e.g., rounded-xl] | [e.g., Friendly, consumer-facing tone] | [Proposed] |
| ... | ... | ... | ... |

---

## Review Checklist

[Run the full checklist — all Locked items must pass]
```

Then: the production code implementation.

---

## Step 0: Context Fitness Check

Before designing, answer these five questions. If the user hasn't provided answers, ask — don't guess on #3 and #5.

| Question | Why it matters | Default if unspecified |
|---|---|---|
| **1. Who is the user?** | Developer vs consumer vs enterprise buyer requires fundamentally different density, language, and visual tone | Assume general consumer |
| **2. What is the primary action?** | Every screen has ONE thing the user should do. The entire hierarchy serves this | Ask — cannot default safely |
| **3. What mood should the UI convey?** | Trust vs energy vs calm vs playfulness drives color temperature, type weight, spacing density, and animation style | Clean and modern (neutral) |
| **4. What device context?** | Mobile-first, desktop-primary, or responsive-all determines layout strategy and touch target sizing | Responsive-all |
| **5. What tech stack?** | React + Tailwind, vanilla HTML/CSS, Vue, Svelte — determines implementation patterns and available primitives | React + Tailwind |

---

## The Four Design Foundations (Establish Before Any Component)

### Foundation 1: Typography System

Typography is 80% of web design. Get this right and the rest follows.

**Type Scale** — Use a consistent ratio. Recommended: **16px base, 1.25 ratio (Major Third)**:

| Token | Size | Use |
|---|---|---|
| `text-xs` | 12px | Captions, metadata, labels |
| `text-sm` | 14px | Secondary text, table cells, helper text |
| `text-base` | 16px | Body text, paragraphs |
| `text-lg` | 18px | Lead paragraphs, emphasized body |
| `text-xl` | 20px | Subsection headings (h4) |
| `text-2xl` | 24px | Section subheadings (h3) |
| `text-3xl` | 30px | Section headings (h2) |
| `text-4xl` | 36px | Page headings (h1) |
| `text-5xl` | 48px | Hero headings |
| `text-6xl` | 64px | Display / landing hero |

**Rules:**
- **Line height**: 1.5 for body, 1.2-1.3 for headings, 1.0-1.1 for display [Locked — readability]
- **Line length**: 60-75 characters max. Use `max-width: 65ch` [Locked — readability research]
- **Font pairing**: Maximum two fonts. One for UI/body, one for headings. More is noise [Recommended]
- **Weight range**: 400 (regular), 500 (medium), 600 (semibold), 700 (bold). Skip extremes [Recommended]
- **Letter spacing**: Tighten headings (-0.02em), body at 0, all-caps at +0.05em [Recommended]
- **Font choice**: Inter, Geist, or system fonts for clean UI. Distinctive fonts (Satoshi, Outfit, GT America) when personality matters [Proposed — user may have brand font]

### Foundation 2: Color Architecture

**System — every interface needs these semantic layers:**

| Layer | Light mode | Dark mode | Purpose |
|---|---|---|---|
| `background` | white | zinc-950 | Base canvas |
| `surface` | zinc-50 | zinc-900 | Cards, panels, elevated areas |
| `border` | zinc-200 | zinc-800 | Dividers, input borders |
| `text-primary` | zinc-900 | zinc-50 | Headings, body text |
| `text-secondary` | zinc-500 | zinc-400 | Labels, captions |
| `text-tertiary` | zinc-400 | zinc-600 | Placeholders, disabled text |
| `primary` | brand color | brand color (adjusted) | CTAs, active states, links |
| `success` | green-600 | green-400 | Confirmations, positive metrics |
| `warning` | amber-600 | amber-400 | Caution states |
| `destructive` | red-600 | red-400 | Errors, delete actions |

**Rules:**
- **3-color rule**: One primary, one neutral scale, one accent. That's the budget for most interfaces [Recommended]
- **60-30-10**: 60% neutral/background, 30% secondary/surface, 10% accent/primary [Recommended]
- **Contrast**: WCAG AA minimum — 4.5:1 for text, 3:1 for large text and UI elements [Locked — accessibility]
- **Dark mode**: Elevated surfaces (zinc-900 → zinc-800 → zinc-700) create depth. Don't just invert [Locked — dark mode breaks otherwise]
- **Never rely on color alone for meaning**: Always pair with text, icon, or shape [Locked — accessibility]

### Foundation 3: Spatial Grid

**Base unit: 4px.** Everything aligns to multiples of 4.

| Token | Value | Use |
|---|---|---|
| `space-1` | 4px | Icon gaps, tight internal padding |
| `space-2` | 8px | Default internal padding, small gaps |
| `space-3` | 12px | Compact component padding |
| `space-4` | 16px | Standard component padding, default gap |
| `space-5` | 20px | Comfortable padding |
| `space-6` | 24px | Section internal spacing |
| `space-8` | 32px | Between related sections |
| `space-10` | 40px | Between distinct sections |
| `space-12` | 48px | Major section breaks |
| `space-16` | 64px | Page section separation |
| `space-20` | 80px | Hero/landing section separation |

**Rules:**
- **Consistent spacing > pixel-perfect spacing.** Two sections with different gaps for no reason is a hierarchy bug [Locked]
- **Container max-width**: 1280px for content, 1440px for full-width. Center with auto margins [Recommended]
- **Page padding**: 16px mobile, 24-32px tablet, 32-64px desktop [Recommended]
- **Grid**: CSS Grid for page layout, Flexbox for component alignment [Recommended]
- **Whitespace is a feature.** When in doubt, add more space. Cramped layouts feel cheap [Recommended]

### Foundation 4: Elevation Strategy

**Choose ONE primary elevation mechanism and commit. Mixing all three looks undesigned.**

| Strategy | When to use | Implementation |
|---|---|---|
| **Borders only** | Dense UIs, dashboards, data-heavy. Clean and systematic | `border border-zinc-200` (light), `border border-zinc-800` (dark) |
| **Subtle shadows** | Consumer apps, landing pages. Feels layered and physical | `shadow-sm` for cards, `shadow-md` for modals, `shadow-lg` for dropdowns |
| **Surface color shifts** | Minimal UIs, dark mode optimized. Quiet and sophisticated | Background → surface → elevated via zinc shade shifts |

**Rules:**
- Borders AND shadows on the same element is visual clutter. Pick one [Locked]
- Dark mode: shadows are near-invisible. Switch to borders or surface shifts [Locked]
- Elevation increases toward the user: page < card < dropdown < modal < toast [Locked — spatial model]

---

## Component Design Patterns

### Buttons

```
Primary:     Filled bg, white text, rounded-lg, px-6 py-3, font-medium
Secondary:   Border only (outline), primary text color, same dimensions
Ghost:       No border, no fill, hover:bg-zinc-100 (subtle highlight)
Destructive: Red variant of primary — ONLY for irreversible actions

States:      default → hover (darken 10%) → active (darken 15%) → focus (ring-2) → disabled (50% opacity)
Sizes:       sm (px-3 py-1.5 text-sm) | md (px-4 py-2 text-sm) | lg (px-6 py-3 text-base)
```

**Rule: ONE primary CTA per viewport.** If everything is primary, nothing is [Locked — hierarchy].

### Cards

```
Container:   bg-white rounded-xl + [elevation strategy] + p-6
Hover:       [elevation increase] + transition (if clickable). Non-clickable cards don't hover
Content:     Image/visual → Title → Description → Metadata → Action
Spacing:     16-24px padding, 12-16px between content blocks
```

### Forms

```
Input:       h-10 px-3 rounded-lg border border-zinc-300 text-sm
             focus:ring-2 focus:ring-primary/20 focus:border-primary
Label:       text-sm font-medium text-zinc-700 mb-1.5 — ABOVE the input, always
Helper:      text-xs text-zinc-500 mt-1
Error:       text-xs text-red-600 mt-1 + border-red-500 on input
Group gap:   24px between form groups
```

**Rule: Labels above inputs, always. Placeholder text is NOT a label** [Locked — accessibility, usability].

### Navigation

```
Top nav:     h-16, sticky top-0, bg-white/80 backdrop-blur-md border-b, z-50
Sidebar:     w-64, fixed left, [surface color], border-r, py-6 px-3
Mobile:      Bottom bar (h-16) for apps, hamburger for sites
Active:      bg-primary/10 text-primary font-medium (sidebar)
             border-b-2 border-primary (top tabs)
```

### Data Display

```
Tables:      text-left, text-sm, divide-y divide-zinc-200
             th: font-medium text-zinc-500 text-xs uppercase tracking-wider py-3
             td: py-4 text-zinc-900
Metrics:     Large number (text-3xl font-semibold) + label below (text-sm text-zinc-500)
             Trend indicator (up/down arrow + percentage + color)
Status:      Colored dot (h-2 w-2 rounded-full) + text label. Never color alone
```

---

## Animation System

### Timing Rules [Locked — perceptual research]

| Duration | Use |
|---|---|
| 100-150ms | Hover/click feedback, button press |
| 150-200ms | Tooltip, dropdown open |
| 200-300ms | Enter/exit transitions, panel expand |
| 300-500ms | Complex transitions, page-level animation |
| Never >500ms | Nothing in UI should take this long |

### Easing [Locked]

- `ease-out` for enters (element arriving — decelerates)
- `ease-in` for exits (element leaving — accelerates)
- `ease-in-out` for position changes
- Never `linear` for UI elements

### Patterns

```css
/* Hover lift — cards, buttons */
transform: translateY(-2px); box-shadow: var(--shadow-md);
transition: transform 150ms ease-out, box-shadow 150ms ease-out;

/* Content entrance — fade up */
@keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } }
animation: fadeIn 200ms ease-out;

/* Loading skeleton */
background: linear-gradient(90deg, var(--surface) 25%, var(--border) 50%, var(--surface) 75%);
background-size: 200% 100%;
animation: shimmer 1.5s infinite;

/* List stagger — 50-75ms per item, max 500ms total sequence */
animation-delay: calc(var(--index) * 50ms);
```

**Rule: Always respect `prefers-reduced-motion`.** Wrap animations in `@media (prefers-reduced-motion: no-preference)` [Locked — accessibility].

---

## Page-Type Design Systems

### Landing Page

| Section | Structure | Key rules |
|---|---|---|
| **Hero** | One headline (5-8 words) + one subheadline (1-2 sentences) + one CTA + one visual | Full viewport or near it. ONE message, ONE action |
| **Social proof** | Logo bar ("Trusted by...") or metric bar ("10K+ users") | Immediately after hero. Reduce buyer anxiety |
| **Features** | 3-column grid (icon + title + description) OR alternating left-right with visuals | Benefits > features. What changes for the user |
| **How it works** | 3-step numbered flow | Reduce perceived complexity |
| **Testimonials** | Quote + name + role + photo | Real people, specific outcomes |
| **Bottom CTA** | Repeat hero CTA with fresh angle | Same action, reinforced |

### Dashboard

| Section | Structure | Key rules |
|---|---|---|
| **Metric cards** | 3-4 across top. Value + label + trend | Most important numbers at a glance |
| **Primary view** | Chart or table — the ONE thing users check daily | Takes most visual weight and space |
| **Filters** | Top bar, left-aligned, with active filter badges | Don't hide filters in dropdowns on dashboards |
| **Empty state** | Illustration + message + CTA to add data | NEVER a blank screen |

### Settings / Form Page

| Section | Structure | Key rules |
|---|---|---|
| **Navigation** | Left sidebar (categories) + right content (form) | Scannable sections |
| **Groups** | Heading + description + fields | Related fields together |
| **Actions** | Sticky footer: Save/Cancel | Or auto-save with status indicator |
| **Danger zone** | Red section at bottom for destructive actions | Confirmation required |

---

## Anti-Patterns — Design Failures and Why They Fail

| Anti-Pattern | Mechanism of Failure | Detection |
|---|---|---|
| Center-aligned body text | Destroys readability — eye loses the left edge on every line return | Squint test: body text looks like a shape, not content |
| >3 font sizes on one component | Fragments hierarchy — reader can't parse relative importance | Count distinct sizes in DevTools |
| Color alone for meaning | ~8% of men are colorblind. Fails WCAG. Invisible to many users | Remove color: does meaning survive? |
| Borders AND shadows on same element | Double-signaling elevation. Looks like a design tool artifact | Visual inspection: does the element have both? |
| Placeholder-only labels | Disappears on focus. Screen readers may miss it. Users forget what field is for | Tab into field: can you tell what it wants? |
| Fixed-width non-responsive layout | Broken on >50% of devices. Immediate credibility loss | Resize to 320px: does it work? |
| Animating everything | Motion sickness risk (vestibular disorders). Performance cost. Users learn to ignore all motion | Remove all animations: what information was lost? |
| Text over busy images without overlay | Unreadable. Contrast fails. Looks accidental | Squint test on the text area |
| Auto-playing carousels | <1% interaction rate. Nobody reads past slide 1. Wastes prime screen real estate | Check analytics: carousel interaction rate |
| Custom scrollbars + custom cursors | Breaks OS-level accessibility settings. Confuses muscle memory | Test with system accessibility zoom |

---

## Review Checklist (Self-Check Before Presenting)

Run this checklist before showing any design output. A "No" on any Locked item is a blocker.

| Check | Type | Pass? |
|---|---|---|
| Squint test: primary element is immediately obvious | Locked | |
| WCAG AA contrast on all text (4.5:1 body, 3:1 large) | Locked | |
| Touch targets ≥44x44px on mobile | Locked | |
| All interactive elements have hover + focus + disabled states | Locked | |
| Data views have loading + empty + error states | Locked | |
| `prefers-reduced-motion` respected | Locked | |
| No hardcoded color/spacing values — all tokens | Locked | |
| Works at 320px viewport width | Locked | |
| Labels on all form inputs (not placeholder-only) | Locked | |
| ONE primary CTA per viewport | Recommended | |
| Consistent elevation strategy (not mixed) | Recommended | |
| Type scale is consistent (no ad-hoc sizes) | Recommended | |
| Spacing follows the 4px grid | Recommended | |
| Animation durations within specified ranges | Recommended | |
| Color system uses ≤3 hues (primary, neutral, accent) | Proposed | |
| Dark mode tested (if applicable) | Proposed | |

---

## Process

When the user requests a UI:

1. **Step 0: Context** — Run the Context Fitness Check. If questions 2 or 3 are unanswered and can't be inferred, ask. Don't guess on primary action or mood.

2. **Establish foundations** — Before any component code, define: type scale, color system, spacing grid, elevation strategy. Present these as the **UI Design Brief** (can be inline code comments or a brief summary before the implementation).

3. **Build mobile-first** — Start at 320px. Layer up with min-width breakpoints.

4. **Implement with tokens** — Every value traces to a design token. No hardcoded hex, px, or magic numbers.

5. **Cover all states** — Every interactive element gets its full state set. Every data view gets loading/empty/error.

6. **Add purposeful motion** — Only animations that communicate. Respect `prefers-reduced-motion`.

7. **Run the review checklist** — Every Locked item must pass. Flag any Recommended items you intentionally skipped and why.

8. **Present with rationale** — Show the code. For key design decisions (color choice, layout direction, typography), add a brief rationale. Flag any Proposed choices the user might want to adjust: "I chose rounded-xl for a friendly feel — change to rounded-md for more professional."

After presenting, offer: "Want me to adjust the color system, layout, spacing density, or any specific component?"
