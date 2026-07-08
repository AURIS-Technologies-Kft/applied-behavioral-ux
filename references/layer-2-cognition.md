# Layer 2 — Cognition: Deep Reference

## Cognitive Load Theory — Applied Checklist

**Sweller (1988, 1994) — Key Effects to Avoid:**

### Split-Attention Effect
When related information is separated spatially (e.g., a diagram with labels on a separate page), cognitive load increases because the user must mentally integrate the pieces.
- **Fix:** Place labels directly on diagrams, put instructions inline with the interface
- **Example:** Form validation messages should appear directly next to the field, not at the top of the page

### Redundancy Effect
Presenting the same information in multiple forms simultaneously can increase load rather than decrease it.
- **Fix:** Don't provide both a text explanation AND an identical audio narration AND a diagram saying the same thing
- **Example:** Don't show a tooltip that repeats the button label. Either show additional info or show nothing.

### Modality Effect
Working memory has separate channels for visual and auditory processing. Using both channels effectively increases total capacity.
- **Fix:** Pair visual instructions with audio cues for complex tasks (e.g., navigation apps combine map visuals with voice instructions)
- **Example:** Show a video tutorial (visual+auditory) rather than a wall of text (visual only)

### Expertise Reversal Effect
Techniques that reduce load for novices can increase load for experts (because experts have already automated the underlying knowledge).
- **Fix:** Allow users to dismiss/skip scaffolding (progressive disclosure handles this naturally)
- **Example:** "Don't show me this again" checkboxes, keyboard shortcuts for power users

## Miller's Law — Practical Chunking Guide

**Original finding:** 7±2 items in working memory. Modern research (Cowan, 2001) suggests the actual capacity is closer to **4±1** chunks.

### Chunking by Context

| Context | Recommended Max | Rationale |
|---|---|---|
| Navigation items | 5-7 | Users scan nav items as chunks |
| Form fields per group | 3-5 | More feels overwhelming |
| Pricing tiers | 3 | Good/Better/Best is the gold standard |
| List items per view | 7-10 | Beyond this, add search/filter |
| Notification categories | 3-5 | More creates notification fatigue |
| Onboarding steps | 3-5 total | Each step should be atomic |
| Feature comparison points | 5-7 | Beyond this, users stop comparing |

### Effective Chunking Strategies
- **Spatial grouping** — Cards, sections, white space
- **Categorization** — Group by user's mental model, not technical architecture
- **Progressive disclosure** — Reveal detail on demand
- **Temporal sequencing** — Step-by-step wizards (but keep total steps ≤ 5)
- **Search** — For large option sets (>20), replace browsing with search + filter

## Mental Models — Identification Guide

**Common user mental models:**

| Domain | User's Mental Model | Design Implication |
|---|---|---|
| File storage | Physical filing cabinet (folders, documents) | Use folder/file metaphor |
| Shopping cart | Physical shopping basket | Cart icon, "add to cart," "checkout" |
| Social media | Physical social gathering | "feed" (like a table), "share," "like" (nod) |
| Email | Physical mailbox | Inbox, sent, drafts, trash |
| Photo management | Physical photo album | Albums, collections, favorites |
| Settings | Physical controls/dials | Toggles, sliders, knobs |
| Search | Physical index/directory | Search bar, results list |
| Calendar | Physical wall calendar | Monthly/weekly view, events as blocks |

**When mental models conflict with your product:**
1. Match the dominant model if possible (lowest friction)
2. If innovating, explicitly teach the new model with a metaphor or analogy
3. Use existing conventions for navigation but innovate in the core interaction
4. Never assume users will "figure it out" — if the model is novel, teach it

**Red flags that your product's model mismatches users:**
- Users click "back" expecting it to undo their last action (not navigate)
- Users look for "save" when the product auto-saves
- Users search for a feature in the place it "should" be, not where you put it
- Users call things by the wrong name (they're using their own model)

## Hick's Law — Choice Optimization

**The Formula:**
`RT = a + b · log₂(n + 1)`
- RT = reaction time
- n = number of choices
- a, b = empirical constants

**Key insight:** The relationship is logarithmic, not linear. The difference between 2 and 4 choices is small. The difference between 2 and 32 choices is large.

### Optimal Choice Counts by Context

| Context | Optimal Choices | Maximum Acceptable |
|---|---|---|
| Primary navigation | 4-7 | 10 (with grouping) |
| Pricing tiers | 3 | 4 (never more) |
| Form dropdowns | 5-7 | 15 (with search) |
| Action menus (contextual) | 3-5 | 10 (with grouping) |
| Settings toggles per page | 5-7 | 15 (with grouping) |
| Notification types | 3-5 | 8 |

### Techniques for Reducing Effective Choice Count
1. **Defaults** — Pre-select the most common option (reduces effective n by 1)
2. **Smart sorting** — Put the most likely choice first (reduces scan time even if n stays the same)
3. **Recommendation** — "We recommend X" (reduces effective choices to 2: the recommended one and "other")
4. **Progressive disclosure** — Show 3-5, with "More options..." for the rest
5. **Categorization** — Group 20 items into 4 categories of 5 items each (effectively 4 choices then 5)

## Information Foraging Theory — Design Patterns

**Pirolli & Card (1999):** Users navigate information systems like animals forage for food — they follow "scent" and optimize for information gained per unit of effort.

### Information Scent Optimization

**What creates strong scent:**
- Descriptive, specific labels ("Upload CSV file" not "Upload")
- Preview text and thumbnails for links
- Clear icons that match expectations
- Breadcrumbs showing path
- Search result snippets with highlighted matches
- Price and availability visible before clicking

**What kills scent:**
- Generic labels ("Learn More," "Click Here," "Submit")
- Mystery meat navigation (icon-only buttons without labels)
- Hidden content behind hover (mobile users can't hover)
- Missing preview images for content
- Vague category names ("Resources," "Solutions")

### Patch Model Application
Users stay in a "patch" (page/section) until the perceived yield drops below the cost of moving to a new patch.

**Design for good patch transitions:**
- Related content suggestions at the bottom of articles (reduces cost of moving)
- Breadcrumbs and persistent navigation (lowers switching cost)
- "Back to results" from detail pages (obvious exit from current patch)
- Content feeds that keep surfacing relevant items (extends the current patch)

### Navigation Cost Reduction
- **Reduce clicks:** Every click between the user and value adds cost
- **Persistent navigation:** Users shouldn't have to scroll to the top to navigate
- **Keyboard shortcuts:** Dramatically reduce navigation cost for power users
- **Predictive navigation:** Suggest where the user might go next (recent items, favorites, frequently visited)
