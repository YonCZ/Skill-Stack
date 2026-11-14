---
name: motion-craft
description: Motion and interaction craft for frontend pages. Use alongside a design skill when a page needs animation, transitions, press feedback, reveals or a signature moment. Does not cover layout, typography or identity.
---

# Motion craft

Motion exists to explain a change or to reward an action. If it does neither, cut it.

## The four questions

Before writing any transition or keyframe, answer these:

1. Should this animate at all? Keyboard actions, high-frequency controls and functional data should not.
2. What is it for: feedback, state change, entrance, or a deliberate moment?
3. What easing? Entering or exiting means ease-out. On-screen movement means ease-in-out. Hover and color changes use ease. Constant motion uses linear.
4. How fast? See the table. UI stays under 300ms.

## Tokens

Start every project with three curves. The browser defaults are too weak.

```css
--ease-out: cubic-bezier(0.23, 1, 0.32, 1);
--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1);
--ease-drawer: cubic-bezier(0.32, 0.72, 0, 1);
```

Never use ease-in for UI. It delays the first frames, which is when the user is watching.

## Duration

| Element | Duration |
|---|---|
| Button press | 100-160ms |
| Tooltip, small popover | 125-200ms |
| Dropdown, select | 150-250ms |
| Modal, drawer | 200-500ms |
| Entrance or signature moment | 400-800ms |

## Rules that carry most of the quality

- Name the property. `transition: transform 200ms var(--ease-out)`, never `transition: all`.
- Animate transform and opacity. Layout properties cause reflow and drop frames.
- Press feedback is immediate: `transform: scale(0.97)` on `:active`, 120-160ms.
- Never animate from `scale(0)`. Start at 0.95 plus opacity.
- Entrances are opacity plus a small translateY. Stagger children by 40-80ms, not by half a second.
- Hover on a card lifts 2px. A photo zooms 1.02 inside its frame, never the frame itself.
- Popovers scale from their trigger origin, not from center.
- Tooltips skip the delay after the first one opens.
- Use CSS transitions for state that can be interrupted. Use keyframes only for one-shot sequences that nothing interrupts.
- Springs for gestures, drag and sheets. Duration curves for everything else.
- Move with the pointer 1:1 during a gesture, then hand off to momentum. Never animate only on release.
- Exit faster than entry. A dismissal should feel immediate.
- Respect `prefers-reduced-motion`: remove transforms and loops, keep opacity changes short.

## Signature moment

Every page gets one moment that carries the product's claim, and only one. It should be tied to a feature, not decoration: a drawing stroke that completes, a measurement that snaps into place, a card that unfolds into its detail. Animate it once, on first view, then leave it still.

## Avoid

- `transition: all`, ease-in for UI, animating width or height, animating `top` or `left`.
- Loops, parallax and marquees on reading surfaces.
- Motion on keyboard-driven actions and on controls used more than once a minute.
- A second signature moment competing with the first.
- Animation used to hide a missing state.
