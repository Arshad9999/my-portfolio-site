# Design System Specification (DESIGN.md)

This contract defines the visual tokens, typography pairings, surface hierarchies, and motion guidelines for the portfolio of Mohammad Arshad Siddiqui.

---

## 1. Color System (Token Architecture)

All colors are defined via root CSS custom properties. The design adheres to a refined warm dark-mode editorial palette with rich obsidian undertones, crisp warm ivory typography, and a signature terracotta/burnt-copper accent.

```css
:root {
  /* Surface Layers */
  --bg-canvas: #0e0e0d;           /* Deep obsidian base */
  --bg-surface: #161615;          /* Card and elevated section background */
  --bg-surface-raised: #1f1f1d;   /* Hover states and floating chrome */
  --bg-subtle: #272724;           /* Subtle containers and tag chips */

  /* Borders & Dividers */
  --border-subtle: rgba(255, 255, 255, 0.08);
  --border-medium: rgba(255, 255, 255, 0.16);
  --border-emphasis: rgba(255, 255, 255, 0.28);

  /* Typography / Text Colors */
  --text-primary: #f5f4ef;        /* High-contrast warm ivory */
  --text-secondary: #c2c0b6;      /* Muted secondary body copy */
  --text-muted: #8e8d85;          /* Metadata, labels, dates */
  --text-disabled: #5a5953;       /* De-emphasized indicators */

  /* Signature Accent (Terracotta / Copper) */
  --accent: #e27042;
  --accent-hover: #f08355;
  --accent-subtle: rgba(226, 112, 66, 0.14);
  --accent-contrast: #ffffff;

  /* Contrast / Inverse */
  --inverse-bg: #f4f3ed;
  --inverse-text: #121211;
}
```

---

## 2. Typography Pairings

- **Display & Headings**: `'Barlow Condensed', -apple-system, sans-serif`
  - Ultra-confident, architectural editorial aesthetic.
  - Weights: `600`, `700`, `800`.
  - Line height: tight (`0.9` to `1.05`).
  - Letter-spacing: `-0.015em` to `0.02em`.
- **Body & Interface**: `'Manrope', -apple-system, BlinkMacSystemFont, sans-serif`
  - Humanist, legible sans-serif with geometric structure.
  - Weights: `400` (body), `500` (medium), `600` (semibold), `700` (bold).
  - Line height: `1.65` for comfortable reading.
- **Monospace & Metadata**: `'JetBrains Mono', ui-monospace, monospace`
  - Used for index numbers (`01 / 05`), code tags, and dates.

---

## 3. Spacing & Spatial Rhythm

Consistent 4px/8px incremental scale:
- `--space-1`: `4px`
- `--space-2`: `8px`
- `--space-3`: `12px`
- `--space-4`: `16px`
- `--space-5`: `24px`
- `--space-6`: `32px`
- `--space-8`: `48px`
- `--space-10`: `64px`
- `--space-12`: `80px`
- `--space-16`: `120px`

Section vertical padding: `clamp(70px, 8vw, 120px)`.
Page gutter horizontal padding: `clamp(20px, 6vw, 80px)`.

---

## 4. Elevation & Borders

- **Border Radii**:
  - Tags / Chips: `4px`
  - Cards & Panels: `10px`
  - Buttons: `6px`
  - Badges / Avatars: `9999px`
- **Focus Rings**:
  - `outline: 2px solid var(--accent);`
  - `outline-offset: 4px;`

---

## 5. Motion Budgets & Transitions

- **Explicit Property Transitions**:
  - `transition: color 180ms ease, background-color 180ms ease, border-color 180ms ease, transform 200ms cubic-bezier(0.16, 1, 0.3, 1);`
  - **No `transition: all`**.
- **Reduced Motion Support**:
  - Respect `@media (prefers-reduced-motion: reduce)`.
