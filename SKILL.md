---
name: applied-behavioral-ux
description: "Research-grounded UX evaluation and design using a 5-layer behavioral science framework — from visual perception to product behavior. Use whenever the user asks to evaluate, design, improve, critique, or audit any user interface, feature, flow, or product experience. Triggers on: UX review, usability critique, conversion optimization, onboarding design, pricing psychology, retention analysis, user psychology, cognitive load assessment, decision architecture, behavioral design, nudge design, or any question about WHY users behave a certain way in a product. Also use when designing screens, flows, or features and the user wants a principled, research-backed approach rather than pure visual aesthetics."
---

# Applied Behavioral UX — 5-Layer Evaluation & Design Framework

A research-grounded framework for evaluating and designing user experiences. Unlike style-focused UX guides, this skill applies peer-reviewed findings from psychology, behavioral economics, and neuroscience directly to product decisions.

## How to Use This Skill

**For evaluation/critique:** Read the task (screenshot, description, code, or flow), then walk through each layer top-to-bottom. For each layer, identify what's working and what violates the principle. End with prioritized recommendations.

**For design/creation:** Walk through each layer bottom-up (Layer 5 → Layer 1) to ground design decisions in behavioral outcomes first, then work back to visual execution.

**For specific problems:** Jump to the relevant layer. If a conversion flow isn't converting, start at Layer 3 (Decision Making). If users aren't finding features, start at Layer 2 (Cognition).

## Framework Overview

```
Layer 1 — Perception (How users SEE)
  Gestalt · Yarbus · Fitts · Visual Hierarchy · Attention
       ↓
Layer 2 — Cognition (How users THINK)
  Cognitive Load · Miller · Mental Models · Hick · Information Foraging
       ↓
Layer 3 — Decision Making (How users CHOOSE)
  Prospect Theory · Loss Aversion · Nudge · Choice Architecture · Cialdini
       ↓
Layer 4 — Motivation (Why users ACT)
  Self-Determination Theory · Goal Theory · Habit Formation · Reinforcement
       ↓
Layer 5 — Product Behavior (What the product DOES)
  Activation · Onboarding · Retention · Conversion · Trust · Pricing
```

---

## Layer 1 — Perception

*How the visual system processes interfaces before conscious thought kicks in.*

### Core Principles

**Gestalt Principles** — The brain groups visual elements automatically based on:
- **Proximity** — Elements close together are perceived as related (use spacing to create groups)
- **Similarity** — Same-colored/styled elements are seen as a set (use for navigation, categories)
- **Continuity** — Eyes follow smooth paths (align elements along visual flow lines)
- **Closure** — The brain completes incomplete shapes (use for icons, illustrations)
- **Figure-Ground** — Users separate foreground from background (ensure clear contrast)
- **Common Fate** — Moving elements together are seen as a group (use for drag interactions)
- **Symmetry** — Symmetrical elements feel unified (use for headers, hero sections)
- **Past Experience** — Recognition overrides grouping (leverage familiar patterns)

**Yarbus' Eye-Tracking Findings** (1967) — Eye movements are task-driven, not random:
- Users' scan paths change dramatically based on their current goal
- A user looking for prices scans completely differently from one evaluating aesthetics
- **Implication:** Design for the primary task, not for "general viewing." Place task-critical elements along predicted scan paths.

**Fitts's Law** (1954) — Time to acquire a target is a function of distance and size:
- `T = a + b · log₂(D/W + 1)` where D = distance, W = target width
- Larger + closer targets are faster to reach
- **Implications:**
  - Primary actions should be large and close to where the user is already looking
  - Click targets should be at least 44×44pt (Apple HIG) / 48×48dp (Material)
  - Place destructive actions far from frequent actions (slow the user down deliberately)
  - Pin important CTAs to edges/corners (they act as "infinite targets")

**Visual Hierarchy** — Users don't "read" interfaces; they scan them in an F-pattern or Z-pattern:
- Most important elements: top-left (start point), largest size, highest contrast
- Secondary: scan-line positions, medium weight
- Tertiary: lower-right, smallest size, reduced contrast
- Use **no more than 3 levels** of visual hierarchy per screen

**Attention** — Selective attention is limited:
- **Von Restorff Effect** — One different element stands out (make the primary CTA the one "different" element)
- **Inattentional Blindness** — Users literally don't see things outside their attention tunnel (don't put critical info next to a busy animation)
- **Change Blindness** — Users miss gradual changes (use obvious transitions for state changes)

### Layer 1 Evaluation Checklist
- [ ] Does the layout follow a natural scan pattern (F or Z)?
- [ ] Are Gestalt groupings used intentionally (not creating false relationships)?
- [ ] Are interactive targets large enough and close enough per Fitts's Law?
- [ ] Is there exactly ONE visually dominant element (the primary action)?
- [ ] Are task-critical elements on predicted eye-scan paths?

---

## Layer 2 — Cognition

*How working memory processes, filters, and navigates information.*

### Core Principles

**Cognitive Load Theory** (Sweller) — Working memory is limited (~4 chunks); manage three types of load:
- **Intrinsic load** — The inherent complexity of the task (minimize by simplifying the task)
- **Extraneous load** — Unnecessary processing from poor design (eliminate: split-attention effect, redundancy effect, clutter)
- **Germane load** — Mental effort dedicated to learning/understanding (maximize: good visualizations, progressive disclosure)
- **Implication:** Every unnecessary element steals capacity from the user's actual goal. Remove decoration. Simplify.

**Miller's Law** (7±2, 1956) — Working memory holds ~7 items (modern research suggests 4±1):
- Chunk information into groups of 3-5 items maximum
- Navigation menus: 5-7 items max per level
- Form fields: group related fields and show one group at a time
- Pricing tiers: 3 options (never more than 4)

**Mental Models** (Johnson-Laird) — Users carry internal representations of how things work:
- Users approach new interfaces with mental models from prior experience
- When the product's model mismatches the user's model → confusion, errors, abandonment
- **Implication:** Design for existing mental models. Use familiar conventions. If innovating, teach explicitly, don't assume transfer.

**Hick's Law** (1952) — Decision time increases logarithmically with the number of choices:
- `RT = a + b · log₂(n + 1)` where n = number of choices
- Going from 2 to 4 choices barely affects time. Going from 4 to 8 choices adds meaningful delay.
- **Implications:**
  - Limit visible choices to 4-7 per decision point
  - Use progressive disclosure for complex option sets
  - Default to smart recommendations to reduce effective choice count
  - categorize and group to reduce perceived complexity

**Information Foraging Theory** (Pirolli & Card, 1999) — Users seek information like animals forage for food:
- **Information scent** — Users assess whether a path will lead to valuable information (use descriptive labels, clear icons, preview text)
- **Patch model** — Users stay in a "patch" until perceived yield drops below cost of moving (ensure deep pages have consistent navigation scent)
- **Navigation cost** — Users minimize cost of finding next valuable item (reduce clicks, provide breadcrumbs, persistent navigation)
- **Implication:** If users can't "smell" the value of a next click, they leave. Every link, button, and nav item must promise clear value.

### Layer 2 Evaluation Checklist
- [ ] Can a first-time user complete the primary task without learning new concepts?
- [ ] Is information chunked into groups of ≤5 items?
- [ ] Does the interface match users' likely mental models?
- [ ] Are choice points limited to ≤7 visible options?
- [ ] Does every link/CTA have strong information scent?
- [ ] Has extraneous cognitive load been eliminated?

---

## Layer 3 — Decision Making

*How users evaluate options, weigh risks, and make choices.*

### Core Principles

**Prospect Theory** (Kahneman & Tversky, 1979) — People evaluate outcomes relative to a reference point, not absolutely:
- **Reference Dependence** — Value is perceived as gain or loss from a reference point (frame prices relative to a competitor or previous price)
- **Loss Aversion** — Losses hurt ~2.25× more than equivalent gains feel good (λ ≈ 2.25). Frame features as "don't lose X" rather than "gain Y" for motivation
- **Diminishing Sensitivity** — The difference between $10 and $20 feels bigger than $100 and $110. Make discounts feel large at the decision point
- **Probability Weighting** — People overweight small probabilities and underweight large ones (highlight rare risks for insurance-type products; emphasize certainty for guarantees)

**Nudge Theory** (Thaler & Sunstein) — Choice architecture that preserves freedom:
- **Defaults** — People stick with defaults. Set the optimal choice as default (e.g., annual billing, recommended plan)
- **Social Proof** — "9 out of 10 people chose…" is more persuasive than feature lists
- **Salience** — Make the right choice obvious (visually prominent recommended tier)
- **Simplification** — Remove friction from the desired path

**Choice Architecture** — How options are presented affects decisions:
- **Decoy Effect (Asymmetric Dominance)** — Add a third option that makes the target look better (pricing tiers with a clearly inferior middle option to push users to premium)
- **Compromise Effect** — Users gravitate toward the middle option (place the profit-maximizing plan in the center)
- **Anchoring** — The first number seen influences all subsequent judgments (show the highest price first, then discount)
- **Paradox of Choice** (Schwartz) — More options → more regret, less satisfaction, often less purchase. Curate, don't catalog

**Cialdini's Principles of Influence** — The 7 levers:
1. **Reciprocity** — Give first (free trial, free content, free tool)
2. **Commitment & Consistency** — Small initial commitments lead to larger ones (start with a free action, escalate)
3. **Social Proof** — Show that others are doing it (testimonials, user counts, activity feeds)
4. **Authority** — Expert endorsements and credentials
5. **Liking** — People buy from people/brands they like (personality, shared identity)
6. **Scarcity** — Limited availability increases value (limited-time offers, waitlists, capacity indicators)
7. **Unity** — Shared identity ("for people like you") — the most powerful and least used principle

### Layer 3 Evaluation Checklist
- [ ] Are outcomes framed relative to a reference point (not just absolute)?
- [ ] Is the default option the one you want users to choose?
- [ ] Is the recommended/preferred option visually salient?
- [ ] Are choices limited to prevent decision paralysis?
- [ ] Is at least one Cialdini principle applied ethically?
- [ ] Does the pricing/choice structure use anchoring or decoy effects?

---

## Layer 4 — Motivation

*What drives sustained engagement and habit formation.*

### Core Principles

**Self-Determination Theory** (Deci & Ryan) — Three innate psychological needs:
- **Autonomy** — Feeling in control. Let users customize, choose, undo. Never trap them.
- **Competence** — Feeling effective. Provide progressive difficulty, clear feedback, skill-building. Make the learning curve gentle.
- **Relatedness** — Feeling connected to others. Social features, community, shared goals, messaging that acknowledges the user as a person.
- Products that satisfy all three → intrinsic motivation. Products that undermine even one → disengagement.

**Goal-Gradient Hypothesis** (Hull, 1932) — Motivation increases as the goal approaches:
- Users accelerate effort when they're close to completion (profile completeness bars, progress indicators)
- Artificial progress: give users a head-start (stamp cards start with 2/10 stamps filled)
- **Implication:** Show progress. Make milestones visible. Celebrate proximity to goals.

**Habit Formation** (Lally et al., 2010; Wood & Neal, 2007) — Habits form through context-dependent repetition:
- Average habit formation: 66 days (range 18-254)
- **Cue → Routine → Reward loop** (Duhigg)
- Context matters more than motivation for maintaining habits (notifications, push, environmental triggers)
- **Implication:** Build triggers into the product. Make the routine effortless. Ensure the reward is variable (see Hook Model).

**Operant Conditioning / Reinforcement** (Skinner) — Behavior shaped by consequences:
- **Positive reinforcement** — Reward desired behavior (celebrate completions, unlock features)
- **Negative reinforcement** — Remove something unpleasant when user acts (dismiss nag screens by upgrading)
- **Avoid punishment** — Never punish users for using the product wrong. Guide instead.
- **Variable ratio schedule** — Unpredictable rewards are most addictive (social media likes, variable content feeds)

**Fogg Behavior Model** (BJ Fogg) — `B = MAP`
- Behavior happens when Motivation, Ability, and a Prompt converge above the action line
- **If motivation is low:** Make the action very easy (one-click, pre-filled)
- **If ability is low:** Boost motivation (urgency, social proof, incentives)
- **If both are present:** Just need a prompt (notification, contextual trigger)
- **Implication:** For every desired behavior, ensure all three elements are present.

### Layer 4 Evaluation Checklist
- [ ] Does the experience support user autonomy (choices, undo, customization)?
- [ ] Is there a visible sense of progress toward a goal?
- [ ] Are there clear triggers (cues) that prompt engagement?
- [ ] Does the product use variable rewards to sustain interest?
- [ ] For every key action: is Motivation × Ability × Prompt all present?
- [ ] Is the product designed for repeated context-dependent use (habit)?

---

## Layer 5 — Product Behavior

*Applying all layers to real product outcomes.*

### Activation (First Value Moment)

The moment a user first experiences the product's core value — this must happen as fast as possible.

**Principles:**
- **Brian Bafour's "Really Good Feature"** — A feature that drives retention must be reachable within the first session. If the core value requires multiple steps, users never arrive.
- **Time-to-Value** — Minimize steps between sign-up and first value delivery. Every additional step loses users.
- **"Aha!" Moment Design** — Engineer a specific moment of product enlightenment. Then optimize the path to reach it faster.

**Design Rules:**
1. Identify the ONE action most correlated with long-term retention
2. Get users to that action within their first session (ideally within 3 minutes)
3. Remove everything between sign-up and that action
4. Pre-fill, pre-configure, use templates — anything to skip setup friction

### Onboarding

**Principles:**
- **Progressive Disclosure** — Teach one concept at a time. Never front-load tutorials.
- **Guided Discovery** — Users learn by doing, not by reading. Guide them through their first real task.
- **Contextual Help** — Help appears when needed, not before. Tooltips on first use of a feature, not on a welcome screen.
- **Commitment Escalation** (Cialdini) — Start with easy commitments (enter name), build to larger ones (connect calendar, invite team). Each step increases investment.

**Design Rules:**
1. Start with the user's goal, not the product's features
2. Maximum 3-5 onboarding steps
3. Each step should deliver value, not just explain
4. Skip "optional" steps — either integrate them or cut them
5. Allow users to skip to the product immediately

### Retention

**Principles:**
- **Hook Model** (Eyal) — `Trigger → Action → Variable Reward → Investment`
  - **Trigger** (external: notification; internal: emotion/need)
  - **Action** (must be easy — Fogg's Ability axis)
  - **Variable Reward** (social validation, information, rewards with variability)
  - **Investment** (user puts something in: data, connections, content — increases return)
- **Switching Costs** — Make leaving harder by increasing stored value (data, connections, reputation, integrations)
- **Engagement Loops** — Create virtuous cycles where using the product makes it more valuable (network effects, personalization, data accumulation)

**Design Rules:**
1. Identify the internal trigger (what emotion/need brings users back?)
2. Make the core action as easy as possible
3. Ensure rewards have variability (not the same result every time)
4. Create investment opportunities (content, settings, connections)
5. Increase switching costs through data and network accumulation

### Conversion

**Principles:**
- Combine Layer 3 (Decision Making) with Layer 2 (Cognition) for maximum effect
- **Friction Audit** — Every field, every click, every page between interest and purchase is conversion leakage. Map the full funnel and count friction points.
- **Anchoring + Social Proof + Scarcity** — The most powerful conversion combo for SaaS pricing

**Design Rules:**
1. Make the free tier valuable enough to create dependence
2. Use value comparison (not feature comparison) for upgrade prompts
3. Trigger upgrade asks at moments of peak engagement (just completed a task successfully)
4. Frame upgrades as "unlocking" not "paying for"
5. Use annual billing defaults with monthly as secondary option

### Trust

**Principles:**
- **Cognitive Trust** — Competence signals (professional design, error-free copy, speed, uptime)
- **Affective Trust** — Warmth signals (personality, helpfulness, acknowledging mistakes)
- **Social Trust** — Authority (experts, certifications) + Social Proof (users, reviews)
- **Transparency** — Clear pricing, honest limitations, visible data handling

**Design Rules:**
1. Professional visual design is a trust prerequisite (Layer 1)
2. Show security signals at moments of data exchange (payment, login)
3. Use real testimonials with names/photos, not vague quotes
4. Be transparent about limitations — honesty builds more trust than polish
5. Error messages should be helpful and human, not technical

### Pricing Psychology

**Principles:**
- **Decoy Effect** — Three tiers with the middle designed to make the premium look like a better deal
- **Anchoring** — Show the most expensive option first, or show the "value" of monthly billing ($X/month → $Y/year, you save $Z)
- **Charm Pricing** — Prices ending in 9 ($19, not $20) still work for lower-price items; less effective for premium products
- **Pain of Paying** (Raworth, 2016) — The psychological discomfort of spending varies by payment method and timing. Annual billing feels less painful per month. "Credits" reduce pain further.
- **Frequency vs. Magnitude** — Many small payments feel worse than one larger payment. Bundle when possible.

**Design Rules:**
1. Three pricing tiers maximum (good / better / best)
2. Highlight the recommended tier visually and with a "Most Popular" badge
3. Anchor prices with the annual equivalent
4. Show what users save by choosing annual
5. Use feature comparison for tiers, but emphasize value stories, not feature lists
6. Include a "contact us" enterprise tier (signals premium, captures leads)

---

## Evaluation Template

When evaluating a product/feature/flow, produce output in this structure:

```
## Layer 1 — Perception
**Score:** [1-5]
**Findings:**
- [What works and what doesn't, referencing specific principles]
**Recommendations:**
- [Prioritized fixes]

## Layer 2 — Cognition
**Score:** [1-5]
...

## Layer 3 — Decision Making
**Score:** [1-5]
...

## Layer 4 — Motivation
**Score:** [1-5]
...

## Layer 5 — Product Behavior
**Score:** [1-5]
...

## Top 3 Actions (Priority Order)
1. [Most impactful change]
2. [Second]
3. [Third]

## Overall Assessment
[2-3 sentence summary of the experience's behavioral effectiveness]
```

## Design Template

When designing a feature/flow, produce output in this structure:

```
## Target Behavior
[What should the user do?]

## Layer 5 → Behavior Strategy
- [Which product behavior pattern applies?]
- [Desired outcome metrics]

## Layer 4 → Motivation Design
- [How does this satisfy autonomy/competence/relatedness?]
- [What triggers cue the behavior?]
- [What rewards reinforce it?]

## Layer 3 → Decision Architecture
- [How is the choice framed?]
- [What's the default?]
- [Which influence principles apply?]

## Layer 2 → Cognitive Design
- [How is information structured (chunking, mental models)?]
- [What's the cognitive load budget?]
- [How strong is the information scent?]

## Layer 1 → Visual Design
- [Scan pattern and hierarchy]
- [Key Gestalt groupings]
- [Fitts's Law target placement]

## Implementation Notes
- [Specific, actionable guidance for implementation]
```

## Ethical Guardrails

This framework describes how human psychology works. Use it ethically:

- **Dark patterns violate Layer 4's Autonomy need** — If a design removes user choice or traps users, it's harmful by this framework's own principles
- **Nudge ≠ Manipulate** — Nudges preserve freedom of choice. If the user can't easily opt out, it's not a nudge
- **Loss aversion is a tool, not a weapon** — Framing legitimate losses is fine. Fabricating losses (false urgency, fake scarcity) is not
- **The Unity principle is about genuine belonging** — Fake tribalism ("us vs them") is weaponized persuasion, not design
- **Variable rewards become addiction when users lose control** — Design for engagement, not compulsion

When evaluating, flag any design that violates these guardrails regardless of its effectiveness.
