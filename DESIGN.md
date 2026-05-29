---
name: A.M Web Studio
description: Websites for Beirut businesses — warm, confident, simple
colors:
  bg: "oklch(98% 0.005 75)"
  surface: "oklch(96% 0.008 70)"
  surface-hover: "oklch(94% 0.01 65)"
  text-primary: "oklch(14% 0.01 70)"
  text-secondary: "oklch(52% 0.015 65)"
  text-muted: "oklch(72% 0.01 60)"
  accent: "oklch(42% 0.08 265)"
  accent-light: "oklch(60% 0.06 268)"
  accent-surface: "oklch(92% 0.02 260)"
  border: "oklch(88% 0.008 65)"
  success: "oklch(50% 0.12 155)"
  hero-bg: "oklch(18% 0.015 260)"
  hero-text: "oklch(96% 0.005 75)"
  hero-muted: "oklch(72% 0.015 255)"
typography:
  display:
    fontFamily: "'Playfair Display', Georgia, 'Times New Roman', serif"
    fontWeight: 600
    lineHeight: 1.15
  headline:
    fontFamily: "'Playfair Display', Georgia, serif"
    fontWeight: 600
    lineHeight: 1.2
  body:
    fontFamily: "'Inter', system-ui, -apple-system, sans-serif"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "'Inter', system-ui, sans-serif"
    fontWeight: 500
    letterSpacing: "0.02em"
    textTransform: "uppercase"
    fontSize: "0.75rem"
rounded:
  sm: "4px"
  md: "8px"
  lg: "16px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "48px"
  xl: "80px"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.hero-text}"
    rounded: "{rounded.sm}"
    padding: "12px 28px"
    fontWeight: 600
  button-primary-hover:
    backgroundColor: "{colors.accent-light}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.hero-text}"
    border: "1px solid {colors.accent}"
    rounded: "{rounded.sm}"
    padding: "12px 28px"
    fontWeight: 600
  button-ghost-hover:
    backgroundColor: "rgba(255, 255, 255, 0.08)"
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  tier-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  tier-card-featured:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
    border: "2px solid {colors.accent}"
---

# Design System: A.M Web Studio

## 1. Overview

**Creative North Star: "The Warm Utility"**

Functional like Stripe or Linear. Warm like a Beirut afternoon. Every pixel serves a purpose, but nothing feels cold or industrial. This is a site that a restaurant owner in Gemmayze can open and immediately trust — not because it's flashy, but because it's clear, fast, and human.

The system uses a restrained warm palette anchored by a deep Mediterranean blue accent, paired with serif display typography over a clean sans body. The result is editorial warmth without sacrificing the crisp, modern feel of a well-built tool.

**Key Characteristics:**
- Warm neutrals (not cool grays) — the background is tinted toward cream, not slate
- One accent color used sparingly — deep warm blue carries CTAs and highlights
- Generous whitespace — every section breathes
- Clean, minimal UI — no decoration, no glassmorphism, no gradient text
- Mobile-first but proportionally generous on desktop

## 2. Colors

A restrained warm palette with a single deep blue accent. Neutrals are tinted toward a warm cream, not cool gray. The accent is a warm-leaning Mediterranean blue — deep enough for confident CTAs, soft enough to feel approachable.

### Primary
- **Warm Blue** (`oklch(42% 0.08 265)`): Primary accent. Used for buttons, links, focus states, selected elements, and the top border of the featured tier card. Never on backgrounds. Never more than 10% of any surface.

### Neutral
- **Warm Cream** (`oklch(98% 0.005 75)`): Page background. The default canvas.
- **Warm Surface** (`oklch(96% 0.008 70)`): Card and section backgrounds. Slightly warmer and deeper than the page background.
- **Warm Surface Hover** (`oklch(94% 0.01 65)`): Hover state for interactive surfaces.
- **Warm Text** (`oklch(14% 0.01 70)`): Primary body text. Dark, warm, not pure black.
- **Warm Muted** (`oklch(52% 0.015 65)`): Secondary text, descriptions, metadata.
- **Warm Subdued** (`oklch(72% 0.01 60)`): Placeholder text, disabled states.
- **Warm Border** (`oklch(88% 0.008 65)`): Subtle dividers, card borders. Almost invisible but present.

### Hero (dark variant)
- **Hero Background** (`oklch(18% 0.015 260)`): Dark warm navy-blue. Not pure black.
- **Hero Text** (`oklch(96% 0.005 75)`): White-ish text on hero. Warm tint.
- **Hero Muted** (`oklch(72% 0.015 255)`): Secondary text on hero.

### Accent Surface
- **Accent Tint** (`oklch(92% 0.02 260)`): Very light blue tint for subtle accent backgrounds.

### Named Rules
**The Sparing Accent Rule.** Warm Blue appears on ≤10% of any viewport. Its rarity is what gives it power. If you find yourself adding a second blue, use a neutral instead.

**The Warm Neutral Rule.** Every neutral carries a trace of warmth (chroma 0.005–0.015 toward yellow/red). If a surface looks gray, it's too cold.

## 3. Typography

**Display Font:** Playfair Display (with Georgia, Times New Roman fallback)
**Body Font:** Inter (with system-ui, -apple-system, sans-serif fallback)

**Character:** The pairing creates a warm editorial feel with modern technical precision. Playfair Display brings heritage and warmth to headings. Inter keeps body text fast, clean, and highly readable at small sizes. The contrast between the two is the point — serif display says "crafted," sans body says "built well."

### Hierarchy
- **Display** (600, `clamp(2.5rem, 6vw, 4.5rem)`, 1.15): Hero headlines only. Never used outside the hero section.
- **Headline** (600, `clamp(1.8rem, 3.5vw, 2.8rem)`, 1.2): Section titles. Left-aligned or centered depending on context.
- **Title** (500, `clamp(1.2rem, 2vw, 1.4rem)`, 1.3): Card titles, tier names, subsection headings.
- **Body** (400, `1rem` (16px), 1.6): All paragraph text. Max line length 70ch.
- **Small** (400, `0.875rem`, 1.5): Captions, metadata, footnotes.
- **Label** (500, `0.75rem`, 1.3, `0.02em` letter-spacing, uppercase): Badges, tags, form labels, small UI text.

### Named Rules
**The No-Scale-Flattening Rule.** Every hierarchy level must contrast from its neighbors by at least one of: weight (≥100), size (≥1.25× ratio), or case (uppercase label vs sentence body). Never flatten the scale.

## 4. Elevation

Flat by default. Surfaces sit on the same plane as the page background, distinguished by the warm surface color and subtle borders (1px, warm border). No shadows at rest.

Shadows appear only as a response to interaction: card hover lifts gently with a soft ambient shadow (`0 8px 30px rgba(0,0,0,0.06)`). This keeps the interface grounded and calm — there's no need to suggest depth when nothing is floating.

## 5. Components

### Buttons
- **Shape:** Gently squared corners (4px). Not sharp, not pill.
- **Primary (Warm Blue):** Filled accent background, white text, 12px 28px padding. Hover: lighter accent background + subtle lift (translateY(-1px)). Transition: 0.2s ease.
- **Ghost (Hero variant):** Transparent, white text, 1px warm blue border. Hover: semi-transparent white background fill. Used on dark hero backgrounds.
- **Outline (Light variant):** Transparent, warm blue text, 1px accent border. Used on light sections.
- All buttons use Inter 600 weight, 1rem size.

### Cards / Tier Cards
- **Corner Style:** Medium rounding (8px).
- **Background:** Warm surface (slightly warmer than page bg).
- **Border:** 1px warm border stroke at rest.
- **Featured tier:** 2px warm blue top border to indicate "most popular."
- **Internal Padding:** 24px (32px on desktop).
- **Shadow Strategy:** No shadow at rest. On hover: soft ambient shadow (`0 8px 30px rgba(0,0,0,0.06)`) + `translateY(-2px)`. Transition: 0.2s ease.

### Menu Card (Demo)
- **Shape:** Medium rounding (8px).
- **Background:** White.
- **Internal Padding:** 28px.
- **Items separated by:** 1px dashed warm border.
- **WhatsApp button:** Solid green (#25d366), white text. Hover: opacity shift. Brand color is intentional here — it matches the WhatsApp brand.

### Contact Links
- **Shape:** Medium rounding (8px).
- **Background:** Semi-transparent white (8%) on hero dark. Subtle border (12% white).
- **Hover:** Background lightens to 14% white + subtle lift.

## 6. Do's and Don'ts

### Do:
- **Do** use warm neutrals everywhere. If it looks gray, it's wrong.
- **Do** use Playfair Display for the hero heading and section titles only.
- **Do** keep the Warm Blue accent to ≤10% of any viewport.
- **Do** use generous whitespace between sections (80px on desktop, 48px on mobile).
- **Do** use `ease-out` transitions with exponential curves (0.2s ease-out).
- **Do** make every interactive element respond with a subtle hover state.

### Don't:
- **Don't** use pure black (#000) or pure white (#fff). Tint every neutral warm.
- **Don't** use gradient text, glassmorphism, or side-stripe borders.
- **Don't** make the site feel like a Wix/Squarespace template. Every card, button, and section must feel custom.
- **Don't** use em dashes. Use commas, colons, or periods instead.
- **Don't** use stock photos of "business people shaking hands."
- **Don't** show hero metrics ("X clients", "Y years"). The work speaks.
- **Don't** animate CSS layout properties (width, height, padding, margin, top, left).
- **Don't** use the hero-metric template (big number + small label + gradient accent).
