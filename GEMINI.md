# Antigravity Web Development Guidelines

Whenever designing, building, refactoring, or reviewing websites, web applications, HTML/CSS/JS, frontend components, or GitHub repositories, Antigravity strictly adheres to the following three foundational open-source design skills:

---

## 1. Hallmark (Nutlope/hallmark)
- **Token Architecture**: Route all colors, font scales, and spacing through CSS variables/tokens (`:root`). Use modern color models (such as OKLCH).
- **Ban on AI Slop**:
  - No generic purple-to-blue gradients or ungrounded glowing ambient blobs.
  - No cards nested inside cards or repetitive 3-box feature grids.
  - No decorative emoji or random icon tiles above every heading.
  - No invented testimonials or fake metric counters.
  - No mandatory eyebrow pill labels above headings.
- **Transitions**: Never use `transition: all`. Always specify explicit properties and timing functions. Respect `prefers-reduced-motion`.
- **Accessibility & Quality**: Minimum WCAG AA contrast (4.5:1), visible high-contrast focus rings (`:focus-visible`), and responsive mobile layouts without horizontal scroll.

---

## 2. Impeccable (pbakaus/impeccable)
- **Typography Diversity**: Avoid default *Inter* for everything. Choose intentional typography pairings (editorial, clean sans, technical mono) suited to the project identity.
- **Surface & Elevation**: Subtle layering, border-radius consistency, and optical alignment over harsh borders and heavy shadows.
- **Design Contracts**: Maintain or reference `DESIGN.md` (tokens, typography, spacing scale) and `PRODUCT.md` (purpose, audience, constraints).
- **Production Loop**: Audit (P0–P3 prioritization) -> Normalize (tokens, radii, rhythm) -> Polish (micro-interactions, states).

---

## 3. Taste Skill (Leonxlnx/taste-skill)
- **Art Direction & Restraint**: Negative space (whitespace) as a primary design asset; clean content-first visual hierarchy.
- **Motion Budgets**: Purposeful micro-interactions with natural easing; avoiding bloated animations or heavy lag-inducing effects.
- **Real-Browser Verification**: Inspect layout balance, typography legibility, and responsiveness across viewports (mobile 390px, tablet 768px, desktop 1280px+).

---

## Skill Cheatsheets
- **Hallmark Skill**: [`.agents/skills/hallmark/SKILL.md`](.agents/skills/hallmark/SKILL.md)
- **Impeccable Skill**: [`.agents/skills/impeccable/SKILL.md`](.agents/skills/impeccable/SKILL.md)
- **Taste Skill**: [`.agents/skills/taste-skill/SKILL.md`](.agents/skills/taste-skill/SKILL.md)
