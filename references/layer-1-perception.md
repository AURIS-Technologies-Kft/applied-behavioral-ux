# Layer 1 — Perception: Deep Reference

## Fitts's Law — Detailed Design Implications

**The Formula:**
`T = a + b · log₂(D/W + 1)`
- T = time to acquire the target
- D = distance from starting point to target center
- W = width of the target along the axis of motion
- a, b = empirical constants (device/input-dependent)

**Key ratios and thresholds (derived from research):**

| Target Size | Typical Usage |
|---|---|
| 44×44 pt (iOS) / 48×48 dp (Android) | Minimum touch target |
| 60×60+ px | Primary CTAs on web |
| 8×16 px minimum | Desktop pointer targets (but aim larger) |

**Practical Applications:**
- **Edge/corner targets:** The cursor stops at screen edges, making them effectively infinite in one dimension. Place primary navigation at screen edges (macOS menu bar, Windows taskbar). Pin primary CTAs to screen edges when possible.
- **Toolbar grouping:** Fitts's Law explains why toolbar items should be close together with generous padding — it reduces D between sequential actions.
- **Destructive actions:** Place Delete, Remove, etc. far from common actions and require deliberate mouse travel (e.g., drag-to-trash, not click-to-delete).
- **Hover targets:** Dropdown menus should have no gaps between trigger and menu items. If the cursor enters the gap, the menu closes (D becomes huge, W becomes tiny).

## Yarbus — Task-Driven Scanning Patterns

**Key Study (1967):** Yarbus had subjects view Repin's painting "The Unexpected Return" while giving them different tasks: estimate material circumstances, determine ages, remember clothing, remember spatial arrangement, etc. Eye movement recordings showed dramatically different scan patterns for each task — despite viewing the same image.

**Scan Patterns for UI:**
- **Information-seeking:** Top-to-bottom, systematic. Users with this goal need clear structure and consistent layout.
- **Evaluative/Comparison:** Side-to-side scanning between alternatives. Place comparison targets symmetrically.
- **Navigational:** Jump to landmarks (logo, nav bar, back button) then follow scent. Clear navigation anchors are essential.
- **Task completion:** Jump to the input/action area directly. Support this with clear form labels and obvious CTAs.

**Design Implication:** You cannot design for "the average scan" because there is none. Design for the primary task. Secondary tasks should be supported but not prioritized.

## Gestalt Principles — Advanced Applications

### Proximity
- Card UIs work because content within the card boundary is proximate
- Whitespace between sections creates natural grouping without borders
- Form field grouping: place related fields within 8-16px of each other, separate groups by 24-32px+

### Similarity
- Color-coding categories: all "warning" elements in amber, all "success" in green
- Navigation items with identical styling are perceived as a set even when spread across the page
- Inconsistent icon styles break similarity and create perceived disorganization

### Continuity
- Left-align body text and form labels — the eye follows a vertical line down
- Horizontal flow in step indicators: 1 → 2 → 3 → 4
- Break continuity intentionally to indicate separate sections or state changes

### Closure
- App icons use this: simplified outlines that the brain completes
- Dotted borders for "add item" zones
- Incomplete circular progress indicators (the brain reads them as a circle with a gap)

### Figure-Ground
- Modal overlays: darkened background (ground), modal (figure)
- Sidebar navigation: collapsed sidebar becomes figure, content becomes ground
- Ensure sufficient contrast between figure and ground — WCAG 4.5:1 for text

### Common Fate
- Animations that move elements together signal they're related
- Drag-and-drop: selected items move in unison
- DON'T animate unrelated elements together — it creates false groupings

### Symmetry
- Login forms centered on page — symmetry creates perceived order
- Two-column feature comparisons use symmetry for direct comparison
- Asymmetry draws attention — use for emphasis, not for layouts

### Past Experience
- Gear icon = settings (even though it looks nothing like physical settings)
- Magnifying glass = search
- Floppy disk = save (even though most users have never seen one)
- When breaking convention, ensure the new pattern is clearly taught

## Attention — Advanced Patterns

### Von Restorff Effect (Isolation Effect)
- In a list of 5 identical items, the one that's different (color, size, shape) is most likely to be remembered
- Application: Primary CTA should be the ONE visually different element on the page
- Warning: If multiple elements are "different," the effect is lost. Use sparingly.

### Inattentional Blindness
- The "gorilla experiment" (Simons & Chabris, 1999): ~50% of observers counting basketball passes failed to notice a person in a gorilla suit walking through
- Application: Don't place critical actions near animated elements, video players, or busy visual areas
- Onboarding tooltips near animated transitions are often completely invisible

### Change Blindness
- Users fail to notice changes between views if the transition is gradual
- Application: Use distinct transitions for state changes (success/error)
- Tab switching with subtle changes often goes unnoticed — use clear visual diffs

### Banner Blindness
- Users have learned to ignore areas that typically contain ads (top banners, right sidebars)
- Application: Don't place critical content in ad-like positions or formats
- If using a banner for legitimate content, make it clearly non-ad (different styling)
