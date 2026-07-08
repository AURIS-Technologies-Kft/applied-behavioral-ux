# Layer 3 — Decision Making: Deep Reference

## Prospect Theory — Applied Framework

**Kahneman & Tversky (1979), Nobel Prize 2002**

### The Value Function
The value function has three critical properties:

1. **Reference Dependence** — Value is perceived as gain/loss relative to a reference point, not in absolute terms
   - Example: A $100 discount on a $500 item feels like a bigger gain than a $100 discount on a $10,000 item, even though the absolute gain is identical
   - Application: Frame discounts relative to the reference price, not in absolute terms. "$200 off" beats "save $200" when the reference is visible

2. **Loss Aversion** (λ ≈ 2.25) — Losses loom approximately 2.25× larger than equivalent gains
   - Example: Losing $50 feels about as bad as gaining $50 feels good × 2.25
   - Application:
     - "Don't lose your work" is more motivating than "Save your work"
     - "You're missing out on [benefit]" is more motivating than "Get [benefit]"
     - Free trial users who lose access after trial end feel the loss more strongly than they felt the trial's value — this drives conversion
     - "Your progress will be lost if you don't upgrade" is ethically questionable but effective

3. **Diminishing Sensitivity** — The marginal value of gains (and losses) decreases
   - Example: The difference between $0 and $100 feels bigger than the difference between $900 and $1000
   - Application: Small discounts on high-price items feel small. Percentage discounts feel better for high prices, absolute discounts for low prices
   - Practical: "$20 off a $100 item" (20%) feels better than "$20 off a $2000 item" (1%)

### The Probability Weighting Function
People systematically misjudge probabilities:
- **Overweight small probabilities** — This is why lottery tickets sell (tiny chance of huge gain feels bigger than it is)
- **Underweight moderate-to-large probabilities** — A 95% chance of success is perceived as less certain than it is
- **Certainty effect** — People disproportionately prefer certain outcomes (100% probability) over near-certain ones (95%)

**Applications:**
- For guarantees: Emphasize certainty ("100% money-back guarantee, no questions asked")
- For risk communication: Make rare risks vivid ("1 in 100" feels different from "1%")
- For subscription cancellation: Highlight what they'll certainly lose (certainty effect) vs. what they might gain by switching

### Framing Effects in UX
The same information framed differently produces different choices:

| Frame A (Gains) | Frame B (Losses) | More Effective When |
|---|---|---|
| "95% success rate" | "5% failure rate" | B is more effective when motivating caution |
| "Save $120/year" | "Don't lose $120/year" | B is ~2× more motivating (loss aversion) |
| "Complete your profile" | "Your profile is 70% complete" | B leverages goal gradient |
| "Upgrade to get X" | "Keep X by upgrading" | B leverages loss aversion |
| "Try free for 14 days" | "Start free — keep your work after trial" | B implies loss avoidance |
| "$10/month" | "$0.33/day" | Daily framing makes the cost feel smaller |

## Nudge Theory — Implementation Patterns

### Default Effects
The most powerful nudge in product design:

| Domain | Effective Default | Impact |
|---|---|---|
| Billing cycle | Annual (not monthly) | 2-3× higher LTV |
| Plan tier | Recommended tier pre-selected | 40-60% choose default |
| Notification settings | Opt-in checkboxes pre-checked (where ethical) | 80-95% keep defaults |
| Privacy settings | Maximum privacy default | Builds trust (but may reduce data) |
| Language/region | Auto-detect from browser/geo | Reduces friction |
| Dark/light mode | Match system preference | Zero friction |

### Social Proof Patterns
- **Normative messaging:** "Most people in your city chose…" > "People chose…"
- **Specificity:** "Join 2,847 designers" > "Join thousands of designers"
- **Activity indicators:** "15 people signed up this week"
- **User avatars:** Real faces in testimonials (not stock photos)
- **Integrations:** "Used by teams at [recognized company logos]"

### Salience
- **Visual prominence:** The recommended option gets the most visual weight
- **Placement:** Put the desired choice in the path of least resistance
- **Timing:** Show upgrade prompts at moments of peak value (just completed a workflow)

### Simplification
- **Pre-fill forms** with reasonable defaults
- **Reduce fields** — every field you remove increases conversion
- **Smart defaults** based on user context (auto-detect timezone, currency, etc.)

## Choice Architecture — Patterns

### Decoy Effect (Asymmetric Dominance)

**Classic Example (The Economist, 2007):**
- Option A: Web-only subscription — $59
- Option B: Print-only subscription — $125
- Option C: Print + Web subscription — $125

When only A and C were offered: 68% chose A (web), 32% chose C (both).
When all three were offered: 16% chose A, 0% chose B, 84% chose C.

The "decoy" (B) made C look like a no-brainer.

**How to implement:**
1. Create your target option (premium tier)
2. Create a decoy that is dominated by the target (same price, fewer features — or same features, higher price)
3. Place the decoy adjacent to the target
4. The target will be chosen significantly more often

### Compromise Effect
Users prefer the middle option when presented with three:
- Tier 1: $9/month — Basic
- Tier 2: $29/month — Pro ← **Most chosen**
- Tier 3: $49/month — Enterprise

**How to implement:**
- Place your profit-maximizing tier in the middle
- Make the top tier expensive enough that it's clearly premium
- Make the bottom tier cheap enough that it's clearly limited

### Anchoring
**Strategic anchoring in pricing:**
1. Show the highest price first (or the "value" of free features)
2. All subsequent prices are judged relative to the anchor
3. Show "Compare to similar services" with higher prices to anchor high
4. For freemium: Show the premium price first, then reveal the free tier

**Anchoring in feature comparison:**
- Lead with the most expensive tier's features
- Users then judge the cheaper tiers as "getting a deal"

## Cialdini's 7 Principles — UX Applications

### 1. Reciprocity
- Free tools (e.g., Canva's free tier creates reciprocity debt)
- Free content / education (builds goodwill)
- "Here's a free resource" before asking for email
- Generous trial periods (30 days feels like a gift)

### 2. Commitment & Consistency
- Start with micro-commitments: create a free account → add one project → invite one team member → upgrade
- Public commitment: "Share your goal" increases follow-through
- Consistency principle: Once users invest time, they want to be consistent by continuing
- Gamification: "You've completed 3 of 5 setup steps" (commitment escalation)

### 3. Social Proof
- "Join 10,000+ teams" on signup page
- Activity feeds showing what others are doing
- Testimonials with specific outcomes ("Increased conversion by 40%")
- Number of users/reviews/downloads visible
- Live user count ("247 people are editing right now")

### 4. Authority
- Expert endorsements ("Recommended by UX designers")
- Certifications and badges (SOC 2, GDPR, "Featured by Apple")
- Data from credible sources ("Research shows…" with citations)
- Professional design itself signals authority

### 5. Liking
- Brand personality that resonates with target users
- Shared identity ("Built for designers, by designers")
- Conversational copy ("Hey there!" vs. "Welcome, User")
- Colors and aesthetics that match user self-image

### 6. Scarcity
- **Time scarcity:** "Offer ends in 24 hours" (use honestly)
- **Quantity scarcity:** "Only 3 spots remaining" (use honestly)
- **Access scarcity:** "Invite-only beta" — creates desire
- **Feature scarcity:** "Premium feature" — limited access
- Warning: Fake scarcity destroys trust (see Layer 5 Trust). Use real scarcity only.

### 7. Unity (Pre-Suasion, Cialdini 2016)
- Shared identity is the most powerful influence lever
- "For people like you" / "Designed for indie hackers"
- Community identity: "Our community of makers"
- In-group language, inside jokes, shared values
- "We're in this together" messaging
- User communities and shared spaces build unity

## Paradox of Choice — Application

**Schwartz (2004):** More choices lead to:
- Decision paralysis (don't choose at all)
- Less satisfaction with the chosen option
- More regret and second-guessing
- Higher switching rates

**Effective curation:**
- Start with 3-5 options, not 20
- Add "More options" for power users (progressive disclosure)
- Use recommendation to reduce effective choice count
- Provide comparison tools for remaining options
- Let users filter, not browse

**Where MORE choice works:**
- When users know exactly what they want (search > browse)
- When differences between options are clear and meaningful
- When users are experts in the domain
