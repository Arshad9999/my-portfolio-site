---
name: taste-skill
description: Frontend art direction, visual taste, and restraint based on Leonxlnx/taste-skill. Enforces Awwwards/Linear-level visual hierarchy, whitespace discipline, motion budgets, and real-browser visual verification.
---

# Taste Skill — Frontend Art Direction & Restraint

Based on [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill).

Taste Skill guides coding agents to produce high-end web interfaces with intentional art direction, spatial discipline, and refined visual aesthetics.

---

## 1. Art Direction & Visual Restraint

1. **Negative Space (Whitespace) as an Active Design Tool**:
   - Generous, deliberate padding gives layouts an elevated, premium feel.
   - Do not crowd content. Allow primary headlines and key imagery to breathe.

2. **Content-First Hierarchy**:
   - Lead with clear, compelling typography and genuine visual assets.
   - Avoid cluttering the screen with unnecessary decorative elements or filler copy.
   - Align elements along deliberate grid lines (e.g., 12-column grids or structured flex columns).

3. **Motion & Interaction Budgets**:
   - Every animation must have a clear functional purpose (feedback, spatial orientation, state transition).
   - Keep transition durations tight (150ms–250ms) with natural easing (e.g., `cubic-bezier(0.16, 1, 0.3, 1)` or standard `ease-out`).
   - Limit heavy canvas shaders, blur filters, or parallax scrolling to avoid compromising performance or battery life.

4. **Visual & Browser Validation**:
   - Validate layouts in a real browser across multiple viewport sizes.
   - Verify that fonts render crisply, line lengths are optimal, and layouts maintain balance on both mobile and desktop screens.
