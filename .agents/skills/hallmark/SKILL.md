---
name: hallmark
description: Anti-AI-slop frontend design skill based on Nutlope/hallmark. Enforces non-waivable Floor rules, design token architecture (OKLCH), job-driven layouts, hero-first construction, and rigorous review gates for web development.
---

# Hallmark — Anti-AI-Slop Web Design Skill

Based on [Nutlope/hallmark](https://github.com/Nutlope/hallmark).

Hallmark ensures that web interfaces are purpose-built, distinct, accessible, and free of generic, repetitive AI-generated tropes ("AI slop").

---

## 1. The Floor (Non-Waivable Rules)

These rules are strict quality gates that must **never** be violated in production code:

1. **Design Token Architecture**:
   - Every color, typography scale, spacing step, border-radius, and elevation must be defined through root CSS custom properties (`:root` / CSS tokens).
   - Prefer modern color models like **OKLCH** (`oklch(L C H)`) or calibrated semantic variables (`--color-bg`, `--color-surface`, `--color-primary`, `--color-text`).
   - **Never** hardcode ad-hoc literal hex codes or arbitrary inline colors across components.

2. **Ban on AI Slop Tropes**:
   - **No cliché purple-to-blue gradients** or ungrounded ambient glowing blobs.
   - **No decorative emoji or generic icons** randomly placed above every section header.
   - **No nested cards inside cards** or repetitive 3-column card grids for every type of information.
   - **No invented metrics, fake testimonials, or placeholder logos** presented as authentic proof.
   - **No mandatory "eyebrow" pill labels** (`<span class="badge">FEATURES</span>`) slapped blindly over every H2.

3. **Motion & Transitions**:
   - **Never** use `transition: all`. Always specify the exact properties being animated (e.g., `transition: color 150ms ease, transform 200ms cubic-bezier(0.16, 1, 0.3, 1)`).
   - Always honor `prefers-reduced-motion: reduce` by dampening or disabling large positional transitions.

4. **Accessibility & Contrast**:
   - Maintain minimum WCAG AA contrast (4.5:1 for body text, 3:1 for large headings and active UI components).
   - Provide clear, high-contrast `:focus-visible` outlines (never remove outlines with `outline: none` without providing an accessible alternative).

5. **Responsive Integrity**:
   - Zero horizontal overflow or horizontal scrollbars at standard mobile viewports (360px, 390px, 412px).
   - Ensure touch targets meet minimum 44×44px sizing for interactive mobile elements.

---

## 2. Job-Driven Layouts

Structure the interface around what the visitor came to accomplish:
- **E-Commerce / Catalog**: Focus on product imagery, specs, pricing, and purchase flows.
- **Tools & SaaS**: Focus on live previews, workflows, inputs, and functional demonstrations.
- **Editorial & Reading**: Focus on comfortable line length (60–75 characters), legible body fonts, and clear typographic hierarchy.
- **Booking & Reservations**: Prioritize dates, availability, tiers, and instant confirmation steps.

Avoid bloated, generic marketing pages that copy-paste: Hero -> 3 Cards -> 3 More Cards -> FAQ -> Giant Footer.

---

## 3. Workflow & Review Gates

1. **Hero Section First**: Build and refine the hero / above-the-fold experience first, verifying contrast and responsiveness across viewports.
2. **Component Discipline**: Ensure secondary components use consistent padding, border-radius, and typographic scales.
3. **Fresh-Context Review**: Before considering a page complete, inspect the rendered layout across viewports (mobile 390px, tablet 768px, desktop 1280px+) to detect visual or layout bugs.
