---
name: applied-behavioral-ux
description: "Research-grounded UX evaluation and design using a 5-layer behavioral science framework — from visual perception to product behavior. Use whenever the user asks to evaluate, design, improve, critique, or audit any user interface, feature, flow, or product experience. Triggers on: UX review, usability critique, conversion optimization, onboarding design, pricing psychology, retention analysis, user psychology, cognitive load assessment, decision architecture, behavioral design, nudge design, or any question about WHY users behave a certain way in a product. Also use when designing screens, flows, or features and the user wants a principled, research-backed approach rather than pure visual aesthetics."
---

# Applied Behavioral UX — 5-Layer Evaluation & Design Framework

A research-grounded framework for evaluating and designing user experiences. Unlike style-focused UX guides, this skill applies peer-reviewed findings from psychology, behavioral economics, and neuroscience directly to product decisions.

## How to Use This Skill

**For evaluation/critique:** If the user provides a URL, browse the live product directly using an agent browser (if available) rather than relying on code or screenshots alone. Observe the actual interface, interactions, and flow as a real user would. Then walk through each layer top-to-bottom. For each layer, identify what's working and what violates the principle. End with prioritized recommendations.

If the user provides a screenshot, description, code, or flow (and no URL or browser is available), walk through each layer using the provided materials.

**For design/creation:** Walk through each layer bottom-up (Layer 5 → Layer 1) to ground design decisions in behavioral outcomes first, then work back to visual execution.

**For specific problems:** Jump to the relevant layer. If a conversion flow isn't converting, start at Layer 3 (Decision Making). If users aren't finding features, start at Layer 2 (Cognition).

## Framework Overview

```
Layer 1 — Perception (How users SEE)
  Gestalt · Yarbus · Fitts · Visual Hierarchy · Attention · Emotional Design · Processing Fluency
       ↓
Layer 2 — Cognition (How users THINK)
  Cognitive Load · Miller · Mental Models · Hick · Information Foraging · Zeigarnik · Flow
       ↓
Layer 3 — Decision Making (How users CHOOSE)
  Prospect Theory · Loss Aversion · Nudge · Choice Architecture · Cialdini · Hyperbolic Discounting
       ↓
Layer 4 — Motivation (Why users ACT)
  Self-Determination Theory · Goal Theory · Habit Formation · Peak-End Rule · Social Identity
       ↓
Layer 5 — Product Behavior (What the product DOES)
  Activation · Onboarding · Retention · Conversion · Trust · Pricing
```

## Mobile Considerations (Cross-Layer)

Mobile is not just "smaller desktop." Several behavioral dynamics are genuinely unique to mobile and affect how all five layers apply.

**Thumb Zone Reachability** (Hoober, 2013; 1,333-person observational study) — 49% of users hold phones one-handed, 36% cradle (one hand holds, other finger taps), 15% use two hands. The thumb is the dominant input mechanism.
- Design for the "natural zone" (center-bottom of screen) for primary actions
- Place frequent actions within easy thumb reach; secondary actions can go in "stretch" zones
- Bottom navigation bars align with thumb ergonomics better than top tabs on phones
- Users shift grip mid-session — designs must be robust to changing grip types

**Divided Attention as Mobile Baseline** — Mobile use frequently occurs while walking, in transit, or in social situations. Desktop use is predominantly stationary and focused.
- Design for degraded cognitive states as the baseline, not as an edge case
- Environmental + digital distractions compound multiplicatively (not additively) to degrade task performance
- Mobile interfaces must work in 30-second attention bursts, not sustained focus sessions

**Screen Size as Natural Progressive Disclosure** (Al-Mushasha et al., 2021; n=1,570) — Counterintuitively, smaller screens produced lower cognitive load than larger screens for the same content. The viewport constrains visible content, reducing extraneous load from information overload and forcing sequential processing.
- Don't try to "fit desktop on mobile" — leverage the natural content limitation
- Mobile's constraint is a feature: it forces progressive disclosure by default
- Related content must appear together on mobile (avoid split-attention from scrolling between diagram and label)

**Smartphone "Mere Presence" Brain Drain** (Ward et al., 2017) — The mere presence of one's own smartphone reduces available cognitive capacity, even when turned off. A desktop computer nearby does not produce this effect.
- Mobile users start with less cognitive capacity before any UI complexity is added
- Simplify mobile interfaces beyond what seems "fair" — the user's cognitive budget is already reduced
- This partially explains why mobile conversion rates are consistently lower than desktop

**Lower Abandonment Cost** — Alternative apps are one tap away in the app store. Desktop users face higher switching costs (download, install, configure).
- Mobile users are less tolerant of friction, slow performance, and confusing flows
- First impression matters more on mobile — users leave faster
- Every step in a mobile flow must justify its existence; there's no patience for "nice to have" steps

### Mobile Evaluation Checklist
- [ ] Are primary actions within easy thumb reach (natural zone)?
- [ ] Does the design work for divided-attention use (transit, walking, multitasking)?
- [ ] Does the mobile layout leverage progressive disclosure naturally (not trying to be desktop)?
- [ ] Is the cognitive load budgeted for reduced mobile capacity (brain drain)?
- [ ] Does every step in the flow justify itself (given low abandonment cost)?

---

Layer 1 — Perception (How users SEE)
  Gestalt · Yarbus · Fitts · Visual Hierarchy · Attention · Emotional Design · Processing Fluency
       ↓
Layer 2 — Cognition (How users THINK)
  Cognitive Load · Miller · Mental Models · Hick · Information Foraging · Zeigarnik · Flow
       ↓
Layer 3 — Decision Making (How users CHOOSE)
  Prospect Theory · Loss Aversion · Nudge · Choice Architecture · Cialdini · Hyperbolic Discounting
       ↓
Layer 4 — Motivation (Why users ACT)
  Self-Determination Theory · Goal Theory · Habit Formation · Peak-End Rule · Social Identity
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

**Yarbus' Eye-Tracking Findings** (1967) — Users' attention is driven by their current goal, not by layout alone:
- A user looking for pricing scans completely differently from one evaluating design quality
- **Implication:** Identify the primary task for each screen and optimize its layout for that task. Use modern research methods (session recordings, heatmaps, click testing) to validate actual scan behavior rather than assuming patterns. Task-critical elements should be immediately findable — place them in expected positions based on user mental models.

**Fitts's Law** (1954) — Time to acquire a target is a function of distance and size:
- `T = a + b · log₂(D/W + 1)` where D = distance, W = target width
- The closer and larger a target is, the faster it is to acquire
- **Implications:**
  - Primary actions should be the most visually prominent interactive element — achieved through contrast (filled vs outlined), color, weight, and spatial emphasis rather than just physical size
  - On touch interfaces, interactive targets must meet platform minimums (44×44pt on iOS, 48×48dp on Android). On desktop, ensure targets are comfortable for pointer precision and adequately spaced
  - Place destructive actions far from frequent actions (slow the user down deliberately)
  - On desktop, persistent navigation in fixed/sticky positions benefits from edge arrest. On touch devices, edges are less accessible — use sticky positioning within thumb zones

**Visual Hierarchy** — Users scan interfaces rather than reading them:
- Scan patterns vary by layout, device, and content type: F-patterns on text-heavy desktop pages, vertical center scanning on mobile single-column, zigzag on comparison pages
- Rather than designing for a specific scan pattern, ensure primary actions and key content are immediately visible above the fold (or at the top of the scroll on mobile)
- Use your typography and spacing system to create clear hierarchy levels — typically 3-5 distinct levels through size, weight, and color contrast

**Attention** — Selective attention is limited:
- **Von Restorff Effect** — A visually distinct element in a set of similar elements is most likely to be noticed. Make the primary CTA the most prominent interactive element through contrast, color, and weight — not through unusual size or shape
- **Inattentional Blindness** — Users literally don't see things outside their attention tunnel (don't put critical info next to a busy animation)
- **Change Blindness** — Users miss gradual changes (use obvious transitions for state changes)

**Emotional Design** (Norman, 2002) — Visual design is not cosmetic; it's functional:
- **Visceral level** — Immediate emotional reaction to appearance (first 50ms). Attractive interfaces trigger positive affect that improves cognitive performance and problem-solving
- **Aesthetic-Usability Effect** (Kurosu & Kashimura, 1995) — Users perceive more attractive interfaces as more usable, even when actual usability is identical. Design investment has measurable ROI
- **Implication:** Beautiful design doesn't just "look nice" — it literally makes users more effective. Never treat visual polish as optional.

**Processing Fluency** (Reber, Winkielman & Schwarz, 1998/2004) — Ease of processing drives preference:
- People misattribute ease of visual processing to aesthetic preference — things that are easy to perceive are experienced as beautiful
- Clean typography, familiar layouts, consistent spacing, and clear hierarchy feel "right" because they process fluently
- **Implication:** Minimalism isn't just a style choice — it leverages a cognitive mechanism. Consistency across a product increases fluency, which increases trust and preference.

**Color Psychology** (Elliot & Maier, 2014) — Color carries meaning and impacts behavior:
- Color effects are context-dependent (Color-in-Context Theory): red signals danger in achievement contexts but attraction in romantic contexts
- Color influences cognition, affect, and behavior in consumer decisions
- **Implication:** CTA colors aren't universal "hacks." Use color strategically to match the emotional tone of the action (green for positive actions, red for warnings/danger, blue for trust/communication)

### Layer 1 Evaluation Checklist
- [ ] Is the layout optimized for the primary task (not just a generic scan pattern)?
- [ ] Are Gestalt groupings used intentionally (not creating false relationships)?
- [ ] Are interactive targets appropriately sized and spaced for both desktop and touch?
- [ ] Is the primary action the most visually prominent interactive element?
- [ ] Are task-critical elements in expected, immediately findable positions?
- [ ] Does the visual design evoke positive emotional response (visceral level)?
- [ ] Is the interface visually consistent enough to leverage processing fluency?
- [ ] Are colors used contextually (not relying on generic "conversion color" myths)?

---

## Layer 2 — Cognition

*How working memory processes, filters, and navigates information.*

### Core Principles

**Conservation of Complexity** (Tesler's Law) — Every application has inherent complexity that cannot be eliminated, only moved:
- Complexity can be moved between the user and the system, but never removed entirely
- Hiding complexity behind a simple interface doesn't eliminate it — it just means the system must be smart enough to handle it
- **Implication:** Before simplifying a UI, ask: "Where did the complexity go?" If the answer is "the user has to figure it out themselves," the design failed. Defaults, automation, and smart suggestions absorb complexity. Removing features without alternative solutions eliminates value, not complexity.

**Cognitive Load Theory** (Sweller) — Working memory is limited (~4 chunks); manage three types of load:
- **Intrinsic load** — The inherent complexity of the task (minimize by simplifying the task)
- **Extraneous load** — Unnecessary processing from poor design (eliminate: split-attention effect, redundancy effect, clutter)
- **Germane load** — Mental effort dedicated to learning/understanding (maximize: good visualizations, progressive disclosure)
- **Implication:** Every unnecessary element steals capacity from the user's actual goal. Remove decoration. Simplify.

**Miller's Law** (7±2, 1956) — Working memory holds ~7 items (modern research suggests 4±1):
- Chunk information into groups of 3-5 items maximum
- Navigation menus: 5-7 items max per level
- Form fields: group related fields and show one group at a time
- Pricing tiers: keep the number of simultaneously visible tiers small (typically 3-4); each tier must have a clear value differentiation

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

**Serial Position Effect** — Items at the beginning and end of a list are remembered best:
- **Primacy effect** — First items receive more attention and are recalled better (first navigation item, top pricing tier, first feature in a list)
- **Recency effect** — Last items also receive disproportionate recall (last nav item, bottom pricing tier, final CTA)
- **Middle items are least remembered** — The middle of any list, menu, or feature set gets the least attention
- **Implication:** Place the most important items first and last in any ordered list. Navigation, pricing tiers, feature comparisons, and error messages all follow this pattern. Never bury critical actions in the middle.

**Mere Exposure Effect** (Zajonc, 1968) — Repeated exposure increases preference, no reward needed:
- Familiar interfaces are preferred partly because of repeated exposure, not just usability
- New design patterns are initially disliked but grow on users with interaction
- **Implication:** Consistency across a product isn't just about learnability — it builds preference through exposure. Don't redesign core patterns frequently.

**Zeigarnik Effect** (1927) — Unfinished tasks are remembered significantly better than completed ones:
- Up to 90% better recall for interrupted/incomplete tasks vs. completed ones
- Creates persistent cognitive tension: "2 of 5 items in cart," "profile 70% complete"
- **Implication:** Use progress indicators, incomplete states, and gentle reminders to drive task completion. But don't overuse — persistent tension becomes anxiety.

**Flow State** (Csikszentmihalyi, 1975) — Optimal experience when challenge matches skill:
- Users enter flow when a task is neither boring (too easy) nor overwhelming (too hard)
- In flow: time distorts, focus is total, performance peaks, satisfaction is high
- **Implication:** Design progressive difficulty. Match default settings to user skill level. Provide clear, immediate feedback to maintain the flow channel. Onboarding should start easy and ramp gradually.

### Layer 2 Evaluation Checklist
- [ ] Can a first-time user complete the primary task without learning new concepts?
- [ ] Is information chunked into groups of ≤5 items?
- [ ] Does the interface match users' likely mental models?
- [ ] Are choice points limited to ≤7 visible options?
- [ ] Does every link/CTA have strong information scent?
- [ ] Has extraneous cognitive load been eliminated?
- [ ] Are the most important items placed first and last in ordered lists (serial position)?
- [ ] Is the experience consistent enough to leverage mere exposure preference?
- [ ] Are there appropriate progress indicators to leverage the Zeigarnik effect?
- [ ] Does the challenge level match the user's skill (flow channel)?
- [ ] Where complexity was removed from the UI — did the system absorb it (Tesler's Law)?

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

**Endowment Effect** (Thaler, 1980/1991) — People value what they own more than what they don't:
- Users demand more to give up a feature/product than they would pay to acquire it
- The mere act of ownership or use increases perceived value
- **Implication:** Free trials, sample accounts, and "try before you buy" create psychological ownership. Losing the product after a trial feels like a loss (interacting with loss aversion). Let users customize and invest during trials to maximize endowment.

**Status Quo Bias** (Samuelson & Zeckhauser, 1988) — People disproportionately stick with defaults:
- Distinct from mere inertia — changing defaults feels like losing something (endowment + loss aversion combined)
- The initial configuration of a product has outsized long-term impact on behavior
- **Implication:** Defaults are the most powerful design tool. Set the optimal choice as default. Make changing settings require deliberate action. The first experience is the permanent experience for most users.

**Regulatory Focus Theory** (Higgins, 1997) — Motivation has two distinct directions:
- **Promotion focus** — Approach gains, ideals, aspirations ("Gain more followers," "Unlock your potential")
- **Prevention focus** — Avoid losses, fulfill duties, prevent problems ("Don't miss important messages," "Protect your data")
- Users shift between states contextually; matching copy to the user's current state doubles effectiveness
- **Implication:** Onboarding and upsell copy should use promotion focus (aspirational). Security, cancellation, and warning copy should use prevention focus. Test both frames for critical conversion points.

**Construal Level Theory** (Trope & Liberman, 2010) — Psychological distance determines abstraction:
- **Near (concrete):** Immediate actions need specific, concrete language ("Click here to add your first task")
- **Far (abstract):** Long-term goals need high-level, value-driven language ("Become more productive")
- Psychological distance can be temporal, spatial, social, or hypothetical
- **Implication:** Future-facing messaging (landing pages, vision, annual plans) should paint abstract value. Immediate actions (CTAs, form fields, onboarding steps) should be painfully concrete and specific.

**Hyperbolic Discounting** (Ainslie, 1975) — Present rewards are overweighted:
- The subjective value of a reward declines hyperbolically with delay — people choose smaller-sooner over larger-later when the smaller reward is immediate
- Explains why users abandon long flows, skip setup, and prefer instant gratification
- **Implication:** Deliver value as fast as possible. Every second of delay between action and reward is conversion leakage. "Instant" previews, immediate feedback, and zero-delay confirmations are not luxuries — they're behavioral necessities.

**Mental Accounting** (Thaler, 1985) — People categorize money into separate "mental accounts":
- A $50 dinner feels different from a $50 monthly subscription, even though it's the same amount — because they come from different mental accounts ("entertainment" vs. "tools")
- Users treat credits, tokens, and virtual currency differently from real money (spending credits feels cheaper than spending cash, even when economically equivalent)
- **Implication:** Frame prices in favorable mental accounts. Annual billing "saves" money per month because users evaluate it against a monthly account. Credits and free trials reduce payment pain by shifting the transaction out of the "real money" account. Bundling works because it moves the total into a single "subscription" account rather than individual purchases.

**Zero Price Effect** (Shampanier, Mazar & Ariely, 2007) — "Free" is not just cheap; it's a qualitatively different category:
- Users disproportionately choose free options over paid ones, even when the paid option is objectively far better value
- The pain of paying drops to zero at $0, creating an irrational preference jump
- **Implication:** Free tiers must be valuable enough to create dependence but not so complete that users never see the need to upgrade. The jump from free to paid is the hardest conversion point — consider "first month free" or "free trial of premium" to bridge the gap, because the psychological distance between $0 and $1 is larger than between $1 and $10.

**Affective Forecasting Errors** (Wilson & Gilbert, 2003) — People systematically mispredict how they'll feel in the future:
- **Impact bias** — Users overestimate how much a feature/product will improve their life (overpromising creates disappointment)
- **Durability bias** — Users overestimate how long positive or negative feelings will last
- **Implication:** Don't overpromise in marketing or onboarding — set realistic expectations. Show concrete, immediate value rather than aspirational transformation. In cancellation flows, users overestimate how good leaving will feel — remind them of what they'll lose (this isn't manipulation; it's helping them make a prediction they're systematically bad at).

### Layer 3 Evaluation Checklist
- [ ] Are outcomes framed relative to a reference point (not just absolute)?
- [ ] Is the default option the one you want users to choose?
- [ ] Is the recommended/preferred option visually salient?
- [ ] Are choices limited to prevent decision paralysis?
- [ ] Is at least one Cialdini principle applied ethically?
- [ ] Does the pricing/choice structure use anchoring or decoy effects?
- [ ] Does the free trial/evaluation create psychological ownership (endowment effect)?
- [ ] Is the copy matching the user's regulatory state (promotion vs. prevention)?
- [ ] Is near-action language concrete and far-action language value-driven (CLT)?
- [ ] Is value delivered immediately or as close to instant as possible?
- [ ] Is pricing framed in favorable mental accounts (mental accounting)?
- [ ] Does the free-to-paid transition bridge the zero price effect gap?
- [ ] Are value promises realistic, not overinflated (affective forecasting)?

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

**Peak-End Rule** (Kahneman et al., 1993) — Experiences are remembered by the most intense moment and the final moment, not by duration:
- Duration neglect: users don't evaluate an experience by how long it took, but by its peak and end
- A single terrible interaction at the end can override months of good experience
- **Implication:** Invest heavily in the "end" of every interaction — success states, completion animations, satisfying closures, thank-you screens. The last touchpoint disproportionately shapes memory and return probability.

**Expectancy-Value Theory** (Eccles & Wigfield, 2000) — Motivation requires both belief in success AND perceived value:
- Users engage when they believe they can succeed (expectancy) AND value the outcome (subjective task value)
- Task value has four components: importance, interest, utility value, and cost (friction)
- **Implication:** Onboarding must establish both "This will be easy" (expectancy) AND "This will be valuable" (value). Removing friction (cost) and demonstrating utility are dual levers. Show a clear path to success before asking for effort.

**Social Identity Theory** (Tajfel & Turner, 1979) — People derive self-esteem from group membership:
- In-group favoritism: users who identify with your product's community show systematic preference and reduced churn
- Shared identity ("designed for designers," community features, team identity) creates attachment that goes beyond functional value
- **Implication:** Community, team identity, and branded language aren't nice-to-haves — they create switching costs through identity, not just data. Users who identify with your product's tribe are significantly harder to switch away from.

**Goal Setting Theory** (Locke & Latham, 1990) — Specific, difficult goals drive higher performance:
- Specific goals consistently outperform vague goals ("write 500 words today" > "write more")
- Goals must be difficult enough to motivate but achievable with commitment and feedback
- **Implication:** Product goals, streaks, and challenges should be specific and moderately challenging. Vague "improve your workflow" goals don't motivate. Pair goals with clear feedback mechanisms and visible progress tracking.

### Layer 4 Evaluation Checklist
- [ ] Does the experience support user autonomy (choices, undo, customization)?
- [ ] Is there a visible sense of progress toward a goal?
- [ ] Are there clear triggers (cues) that prompt engagement?
- [ ] Does the product use variable rewards to sustain interest?
- [ ] For every key action: is Motivation × Ability × Prompt all present?
- [ ] Is the product designed for repeated context-dependent use (habit)?
- [ ] Are the "peak" and "end" moments of every flow deliberately designed?
- [ ] Does the experience establish both expectancy ("I can do this") and value ("This matters")?
- [ ] Does the product foster social identity / community belonging?
- [ ] Are goals specific and moderately challenging (not vague)?

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
1. For tiered pricing, 3 tiers is the most common and well-understood structure. The optimal number depends on your market and pricing model — usage-based products may not fit neatly into 3 tiers. What matters is that each tier has a clear, distinct value story
2. Visually distinguish the recommended tier — through subtle design treatment (highlighted border, elevated shadow, slightly larger scale, or prominent position). Avoid heavy-handed badges; many modern products let visual hierarchy speak for itself
3. Anchor prices with the annual equivalent
4. Show what users save by choosing annual
5. Use feature comparison for tiers, but emphasize value stories, not feature lists
6. Include a "contact us" enterprise tier (signals premium, captures leads)

---

## Evaluation Template

When evaluating a product/feature/flow, browse the live interface if a URL is available (using an agent browser). Observe the actual experience as a user would — navigation, interactions, responsive behavior, loading states, and flow completion. Then produce output in this structure:

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
