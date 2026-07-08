# Layer 4 — Motivation: Deep Reference

## Self-Determination Theory — Design Patterns

**Deci & Ryan (1985, 2000)** — Three basic psychological needs that drive intrinsic motivation:

### Autonomy
The need to feel in control of one's own behavior and goals.

**Autonomy-Supportive Design:**
| Pattern | Example |
|---|---|
| Meaningful choices | Let users choose their theme, layout, workflow |
| Voluntary action | Never force actions; always provide an "opt out" |
| Transparency | Explain WHY, not just WHAT. "We ask for your email to send your receipt" |
| Undo/Redo | Every destructive action should be reversible |
| Customization | Let users tailor the experience to their preferences |
| No dark patterns | If users feel trapped, autonomy is violated |

**Autonomy Violations (Avoid):**
- Mandatory interstitials that can't be dismissed
- Forced social sharing to access features
- No way to delete account or data
- Hard-coded defaults that can't be changed
- "Are you sure you want to leave?" on every page exit
- Mandatory tutorial that can't be skipped

### Competence
The need to feel effective and capable.

**Competence-Supportive Design:**
| Pattern | Example |
|---|---|
| Progressive difficulty | Start simple, add complexity as user masters basics |
| Clear feedback | Immediate, specific feedback on every action |
| Skill-building | Tutorials that teach transferable skills |
| Achievement signals | Badges, streaks, levels (but tied to real accomplishment) |
| Metrics/progress | "You've written 5,000 words this week" |
| Success states | Celebrate completions, milestones, streaks |

**Competence Violations (Avoid):**
- Overwhelming first-time users with advanced features
- No feedback when actions succeed ("Did it work?")
- Error messages that blame the user
- Inconsistent behavior (same action, different result)
- Impossible tasks with no guidance

### Relatedness
The need to feel connected to others and belong.

**Relatedness-Supportive Design:**
| Pattern | Example |
|---|---|
| Social features | Comments, mentions, shared workspaces |
| Community | Forums, user groups, community events |
| Human voice | Conversational copy, personalized messages |
| Shared goals | Team dashboards, collaborative projects |
| Acknowledgment | "Thanks for your feedback" — real human response |
| User identity | Profiles, avatars, personalization |

**Relatedness Violations (Avoid):**
- Cold, robotic language everywhere
- No way to contact a human
- Ignoring user feedback
- Zero social features in a social product
- Anonymous, faceless product with no personality

### The Motivation Continuum

SDT describes a spectrum from extrinsic to intrinsic motivation:

```
Amotivation ← External Regulation ← Identified Regulation ← Integrated Regulation → Intrinsic Motivation
   (no motive)    (rewards/punishment)  (personal value)    (self-concordant)      (inherent enjoyment)
```

**Design goal:** Move users rightward on this spectrum.

**How:**
- External → Identified: Help users see personal value ("This saves you 2 hours/week")
- Identified → Integrated: Make the behavior part of user identity ("You're the organized one on the team")
- Integrated → Intrinsic: Make the process itself enjoyable (smooth interactions, delightful moments)

## Goal-Gradient Hypothesis — Detailed Applications

**Hull (1932), Nunes & Drèze (2006):** Motivation increases as distance to the goal decreases.

### Key Findings
- Effort accelerates nonlinearly as the goal approaches
- The effect works even with artificial progress (loyalty cards with 2/10 stamps pre-filled vs. 0/10)
- Progress visualization increases motivation even when actual progress is the same

### Design Patterns

**1. Progress Bars**
- Profile completion: "80% complete — add a photo to finish"
- Multi-step flows: "Step 3 of 4"
- Course/learning progress: visual bar + percentage
- Gamification: XP bars, level progress

**2. Artificial Head-Starts**
- Loyalty programs: Pre-stamp cards
- Free tier: Give enough value that the "goal" (full value) feels close
- Freemium: "You're 1 step away from Pro features"

**3. Milestone Celebration**
- Celebrate at 25%, 50%, 75%, 100%
- Each celebration resets the "recent progress" anchor
- "You've reached Level 5! Only 2 more to unlock…"

**4. Sub-Goals**
- Break large goals into visible sub-goals
- Each sub-goal reached creates a new goal-gradient effect
- "Complete your profile" → "Add your first project" → "Invite a teammate" → "Customize your dashboard"

## Habit Formation — Applied Framework

**Lally et al. (2010), Wood & Neal (2007), Duhigg (2012)**

### The Habit Loop (Duhigg)

```
CUE → ROUTINE → REWARD → CRAVING (repeat)
```

**Cue Triggers in Product Design:**
| Cue Type | Example |
|---|---|
| Time-based | Daily digest emails at 9am |
| Location-based | Push notification when near store |
| Emotional | "Feeling stressed? Try a 2-minute meditation" |
| Sequential | After completing task A, prompt for task B |
| Social | "5 friends updated their status" |
| External event | New email received, calendar event approaching |

**Routine Design Principles:**
- Make the routine as easy as possible (Fogg's Ability)
- Reduce steps between cue and reward
- Make the routine the path of least resistance
- Support multiple entry points (don't require a specific sequence)

**Reward Types:**
| Reward Type | Example | Strength |
|---|---|---|
| Fixed reward | Points for every action | Predictable, good for learning |
| Variable reward | Social likes, random content | Addictive, sustains engagement |
| Social reward | Comments, reactions, shares | Powerful, leverages relatedness |
| Achievement reward | Badges, levels, streaks | Competence-satisfying |
| Information reward | New data, insights, discovery | Curiosity-satisfying |

**Variable Rewards — The Hook Model Integration (Eyal):**
1. **Variable social rewards** — Content from other people (social media feeds, comments)
2. **Variable information rewards** — New information, search results, data updates
3. **Variable material rewards** — Points, rewards, prizes with unpredictable outcomes

### Building Investment (The Fourth Phase of the Hook)
Investment increases the likelihood of the next trigger:
- **Data investment** — Users add data that makes the product more valuable (playlists, contacts, preferences)
- **Social investment** — Users build connections that are costly to leave (networks, teams, followers)
- **Reputation investment** — Users earn status that they don't want to lose (ratings, karma, streaks)
- **Configuration investment** — Users customize settings that represent effort (dashboard layout, notifications)

### Habit Formation Timeline
| Timeframe | Focus | Key Metric |
|---|---|---|
| Day 1 | First value moment | Activation rate |
| Day 1-7 | Repeat engagement | D7 retention |
| Day 7-30 | Habit formation | D30 retention |
| Day 30+ | Habit strength | D90 retention, engagement frequency |

## Fogg Behavior Model — Implementation Guide

**BJ Fogg, Stanford Persuasive Technology Lab**

### The Formula
`B = MAP` — Behavior happens when Motivation, Ability, and Prompt converge above the Action Line.

### The Behavior Grid
Fogg classifies behaviors by duration and whether they're new or familiar:

| | One-Time | New Habit | Familiar Habit |
|---|---|---|---|
| **Dot** (small) | Install app | Drink water daily | Check email |
| **Span** (over time) | Onboarding | Exercise routine | Commute to work |
| **Path** (permanent) | Buy house | Eat healthy | Brush teeth |

**Design implication:** Match your intervention to the behavior type.
- One-time behaviors: High motivation needed briefly (launch campaign)
- New habits: Start with easy actions, build up
- Familiar habits: Need consistent prompts (notifications)

### The Action Line
Below a certain threshold of combined Motivation + Ability, no Prompt will trigger behavior.

**Three Paths to Behavior:**

1. **Motivation is high →** Prompt the behavior. User will act even if it's somewhat hard.
   - Use: Onboarding (users are motivated when signing up)
   - Design: Capitalize on this window with clear next steps

2. **Motivation is moderate →** Make it easy. Increase Ability.
   - Use: Core feature adoption
   - Design: Reduce clicks, pre-fill, use templates, offer shortcuts

3. **Motivation is low →** Make it very easy AND prompt at the right moment.
   - Use: Retention/engagement
   - Design: Push notifications with deep links (one tap to action), widgets, quick actions

### Ability Levers (Ordered by Effectiveness)
| Lever | Effectiveness | Example |
|---|---|---|
| Time | ★★★★★ | Reduce time required (instant actions) |
| Money | ★★★★ | Reduce or eliminate cost (freemium) |
| Physical effort | ★★★★ | Reduce clicks, typing, navigation |
| Brain cycles | ★★★ | Reduce cognitive load (defaults, auto-fill) |
| Social deviance | ★★ | Make the behavior socially normal (social proof) |
| Non-routine | ★ | Make the behavior habitual (triggers) |

### Prompt Types
| Type | Example | Best For |
|---|---|---|
| Spark (direct prompt) | "Upgrade now" button | When motivation is present |
| Facilitator (ability prompt) | "One-click to complete setup" | When motivation is moderate |
| Signal (behavior prompt) | "New message" notification | When behavior is familiar |
