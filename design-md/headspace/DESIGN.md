# Headspace Design System

> Warm, friendly mindfulness design built around a sunny orange, soft rounded shapes, and playful character illustration. Headspace's public brand makes mental health feel approachable, using cheerful colors, generous rounding, and gentle motion instead of clinical minimalism.

---

## 1. Visual Theme & Atmosphere

### Overall Aesthetic
Headspace feels like **a kind friend with a sketchbook**. Round, blobby characters, warm orange and yellow tones, and soft cream surfaces make meditation feel light and welcoming.

### Mood & Feeling
- Warm, kind, and reassuring
- Playful and optimistic
- Calm without being sleepy
- Approachable and non-judgmental
- Joyful and human

### Design Density
**Low density.** Large illustrations, big rounded cards, and short copy keep every screen easy to take in.

### Visual Character
- Headspace orange (`#FF7E1D`-adjacent) as the core brand color
- Cream/off-white (`#FFF9F2`-adjacent) canvases
- Round, simple character illustrations with flat colors
- Highly rounded cards and pill buttons
- Blue (`#0061EF`-adjacent) as a secondary action color

---

## 2. Color Palette & Roles

### Core Foundation

| Token | Hex | Role |
|-------|-----|------|
| `--hs-orange` | `#FF7E1D` | Primary brand, hero accents |
| `--hs-blue` | `#0061EF` | Primary CTA buttons, links |
| `--hs-blue-dark` | `#0050C8` | CTA hover state |
| `--hs-cream` | `#FFF9F2` | Warm canvas |
| `--hs-white` | `#FFFFFF` | Card surfaces |
| `--hs-ink` | `#2D2C2B` | Primary text |

### Support Palette

| Token | Hex | Role |
|-------|-----|------|
| `--hs-ink-muted` | `#63605D` | Secondary text |
| `--hs-yellow` | `#FFCE00` | Illustration, highlight |
| `--hs-pink` | `#FF8FA3` | Illustration, sleep/kids content |
| `--hs-purple` | `#5A3FC0` | Sleep content, night mode |
| `--hs-green` | `#3DB88B` | Movement/focus content |
| `--hs-navy` | `#1B1B3A` | Sleep dark surfaces |
| `--hs-border` | `#EBE6E0` | Dividers, input borders |

---

## 3. Typography Rules

### Font Stack

```css
--font-display: "Headspace Apercu", "Apercu", "Helvetica Neue", Arial, sans-serif;
--font-sans: "Headspace Apercu", "Apercu", -apple-system, BlinkMacSystemFont, sans-serif;
```

### Type Scale

| Element | Size | Weight | Line Height | Letter Spacing | Color |
|---------|------|--------|-------------|----------------|-------|
| Marketing Hero | 56px | 700 | 1.1 | -0.02em | `#2D2C2B` |
| Section Heading | 36px | 700 | 1.2 | -0.01em | `#2D2C2B` |
| Card Title | 20px | 700 | 1.3 | 0 | `#2D2C2B` |
| Body | 18px | 400 | 1.55 | 0 | `#2D2C2B` |
| Meta (duration) | 14px | 500 | 1.4 | 0 | `#63605D` |
| Button Label | 16px | 700 | 1.2 | 0 | `#FFFFFF` |

### Typography Philosophy
Type is **friendly and rounded in spirit** — a geometric-humanist sans with bold headlines and comfortable body sizes that feel conversational.

---

## 4. Component Stylings

### Buttons

```css
.button-primary {
  background: #0061ef;
  color: #ffffff;
  border: none;
  border-radius: 999px;
  min-height: 52px;
  padding: 0 32px;
  font-size: 16px;
  font-weight: 700;
}

.button-primary:hover {
  background: #0050c8;
}

.button-secondary {
  background: transparent;
  color: #2d2c2b;
  border: 2px solid #2d2c2b;
  border-radius: 999px;
  min-height: 52px;
  padding: 0 32px;
}
```

### Content Card

```css
.content-card {
  background: #ffffff;
  border-radius: 24px;
  overflow: hidden;
}

.content-card-art {
  aspect-ratio: 1 / 1;
  background: #ff7e1d;
  display: grid;
  place-items: center;
}

.content-card-body {
  padding: 16px 20px 20px;
}
```

### Play Button

```css
.play-circle {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  background: #ffffff;
  color: #2d2c2b;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
}
```

### Component Notes
- Content cards pair a solid-color illustration tile with short title and duration
- Session players feature a large centered animated character
- Progress uses soft rounded rings rather than bars
- Sleep content switches to navy/purple night surfaces

---

## 5. Layout Principles

### Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps |
| `--space-2` | `8px` | Meta spacing |
| `--space-3` | `16px` | Card padding |
| `--space-4` | `24px` | Grid gaps |
| `--space-5` | `64px` | Section spacing |
| `--space-6` | `120px` | Hero spacing |

### Layout Behavior
- Marketing heroes pair a big headline with a large character illustration
- Content grids use 2–4 columns of rounded cards
- Pricing shows two plans side by side with the annual plan highlighted

### Whitespace Philosophy
Whitespace should feel **like a deep breath** — open, soft, and unhurried.

---

## 6. Depth & Elevation

### Elevation Strategy
Headspace is **soft and mostly flat**, using color blocks and rounding for hierarchy, with gentle shadows only on floating controls.

```css
--shadow-soft: 0 4px 16px rgba(0, 0, 0, 0.08);
--shadow-float: 0 8px 32px rgba(0, 0, 0, 0.12);
```

### Surface Hierarchy
- Warm cream canvas
- White and solid-color rounded cards
- Floating play controls and modals

---

## 7. Do's and Don'ts

### Do
- Use orange and warm tones to convey kindness
- Round everything generously (cards 24px, buttons pill)
- Use simple flat character illustrations
- Keep copy short, warm, and encouraging

### Don't
- Do not use sharp corners or harsh contrast
- Do not use clinical grays or cold whites as the main canvas
- Do not use photographic stock imagery in place of illustration
- Do not crowd screens with dense information

---

## 8. Responsive Behavior

### Breakpoints

| Breakpoint | Width | Behavior |
|------------|-------|----------|
| Mobile | `< 768px` | Single-column cards, full-width pill buttons |
| Tablet | `768px - 1023px` | Two-column card grids |
| Desktop | `1024px+` | Three-to-four column grids, side-by-side hero |

### Responsive Rules
- Pill buttons are at least 48px tall on touch devices
- Illustrations scale but stay prominent above the fold
- Horizontal carousels replace grids on mobile

---

## 9. Agent Prompt Guide

### Quick Reference
- Warm orange brand with blue pill CTAs
- Cream canvas, highly rounded cards
- Flat, round character illustrations
- Friendly, calm, encouraging tone

### Prompt Template
```text
Design this like Headspace's current public brand and product style:
- warm cream canvas with Headspace orange (#FF7E1D) brand accents
- blue (#0061EF) pill-shaped primary buttons
- highly rounded (24px) cards with solid-color illustration tiles
- simple, flat, round character illustrations
- bold friendly sans headlines with comfortable 18px body text
- warm, kind, playful mindfulness atmosphere
```
