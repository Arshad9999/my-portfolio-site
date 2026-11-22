---
name: impeccable
description: Design vocabulary, architectural constraints, and anti-slop detector rules based on pbakaus/impeccable. Enforces typography diversity (avoiding default Inter), calibrated color palettes, component discipline, and the 3-step Audit/Normalize/Polish workflow.
---

# Impeccable — Frontend Craft & Design Vocabulary

Based on [pbakaus/impeccable](https://github.com/pbakaus/impeccable).

Impeccable equips agents with a precise design vocabulary and deterministic anti-slop detector rules to deliver polished, human-grade user interfaces.

---

## 1. Core Principles & Anti-Slop Guidelines

1. **Typography Selection**:
   - **Avoid default Inter for everything**. Inter is the statistical default of AI-generated interfaces.
   - Choose typography that reflects the project's character:
     - Editorial / Literary: Playfair Display, Merriweather, Newsreader, Georgia.
     - Technical / Developer: JetBrains Mono, Fira Code, IBM Plex Sans / Mono.
     - Clean & Modern: Plus Jakarta Sans, Geist, Satoshi, General Sans, Outfit.
     - Friendly / Humanist: DM Sans, Urbanist, Figtree.
   - Maintain strict typographic scales (H1, H2, H3, Body, Small) with intentional line heights (`leading-tight` for headings, `leading-relaxed` for long prose).

2. **Color Palette & Surface Layering**:
   - Build surfaces with subtle depth and elevation rather than harsh borders or gratuitous drop-shadows.
   - Avoid low-contrast light-gray text on white or dark-gray text on black. Ensure crisp contrast.
   - Use accents sparingly for focal points (primary CTAs, status badges, active indicators).

3. **Component Hierarchy & Restraint**:
   - Avoid monotonous "card fatigue" (wrapping every piece of text, icon, and button in its own boxed card).
   - Use whitespace, subtle divider rules, or typography size shifts to demarcate sections naturally.
   - Avoid rounded-square colored background icon tiles above every heading.

---

## 2. Design System Contracts (`DESIGN.md` & `PRODUCT.md`)

When starting or maintaining a website or UI application:
- **`PRODUCT.md`**: Define the core product goals, target audience, primary user actions, and technical constraints.
- **`DESIGN.md`**: Define design tokens:
  - Color palette (backgrounds, surfaces, borders, primary, muted text).
  - Typography scale & font family pairings.
  - Spacing scale (4px, 8px, 12px, 16px, 24px, 32px, 48px).
  - Border radii scale (subtle: 4px/6px, modern: 8px/12px, pill: 9999px).

---

## 3. The 3-Step Production Design Loop

When creating or modifying UI:

1. **Audit**:
   - Evaluate accessibility (contrast, aria attributes, focus rings).
   - Evaluate responsiveness (flex/grid wrapping, padding adaptation).
   - Categorize issues strictly from **P0 (Blocker)** to **P3 (Visual Polish)**.

2. **Normalize**:
   - Ensure all components reference the project's design tokens in `DESIGN.md`.
   - Harmonize border-radii, font weights, and spacing across buttons, inputs, and panels.

3. **Polish**:
   - Add purposeful micro-interactions (smooth hover state transitions, active press effects, crisp loading skeletons).
   - Ensure reduced-motion media queries are honored.
