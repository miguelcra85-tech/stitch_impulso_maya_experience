---
name: Impulso Maya VR
colors:
  surface: '#0c1519'
  surface-dim: '#0c1519'
  surface-bright: '#323a3f'
  surface-container-lowest: '#070f13'
  surface-container-low: '#141d21'
  surface-container: '#182125'
  surface-container-high: '#232b30'
  surface-container-highest: '#2d363b'
  on-surface: '#dbe4ea'
  on-surface-variant: '#bbc9cf'
  inverse-surface: '#dbe4ea'
  inverse-on-surface: '#293236'
  outline: '#859398'
  outline-variant: '#3c494e'
  surface-tint: '#3cd7ff'
  primary: '#a8e8ff'
  on-primary: '#003642'
  primary-container: '#00d4ff'
  on-primary-container: '#00586b'
  inverse-primary: '#00677e'
  secondary: '#b9c7e4'
  on-secondary: '#233148'
  secondary-container: '#394760'
  on-secondary-container: '#a8b5d2'
  tertiary: '#c9e2f3'
  on-tertiary: '#1b3340'
  tertiary-container: '#adc6d6'
  on-tertiary-container: '#3b5361'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#b4ebff'
  primary-fixed-dim: '#3cd7ff'
  on-primary-fixed: '#001f27'
  on-primary-fixed-variant: '#004e5f'
  secondary-fixed: '#d6e3ff'
  secondary-fixed-dim: '#b9c7e4'
  on-secondary-fixed: '#0d1c32'
  on-secondary-fixed-variant: '#394760'
  tertiary-fixed: '#cde6f7'
  tertiary-fixed-dim: '#b1cada'
  on-tertiary-fixed: '#031e2a'
  on-tertiary-fixed-variant: '#324a57'
  background: '#0c1519'
  on-background: '#dbe4ea'
  surface-variant: '#2d363b'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '800'
    lineHeight: 56px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Inter
    fontSize: 36px
    fontWeight: '800'
    lineHeight: 42px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-caps:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.1em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  container-padding-mobile: 20px
  container-padding-desktop: 64px
  gutter: 16px
  stack-sm: 12px
  stack-md: 24px
  stack-lg: 48px
---

## Brand & Style

The design system is engineered to transport users into a high-fidelity virtual representation of Mayan heritage, blending the deep mysteries of the ocean with the precision of space exploration. The brand personality is **visionary, immersive, and serene**. It targets luxury travelers and tech enthusiasts seeking a "phygital" escape.

The aesthetic follows a **Deep-Sea Glassmorphism** style. It utilizes high-transparency layers, vibrant backdrop blurs, and luminous accents to simulate looking through water or a spacecraft visor. Every interaction should feel like navigating a sophisticated holographic interface—fluid, responsive, and weightless.

## Colors

The palette is anchored in the deep shadows of the Yucatán cenotes and the brilliance of tropical horizons.

*   **Primary (Cian Vibrante):** Used for interactive states, progress indicators, and "energy" focal points. It should appear to emit light.
*   **Secondary (Azul Profundo):** The foundation of the UI. Used for background depths and base canvases.
*   **Tertiary (Azul Acero):** Utilized for secondary text, borders, and inactive UI elements to provide a metallic, tech-driven contrast.
*   **Neutral (Blanco Cristalino):** Reserved for high-priority typography and icons to ensure maximum legibility against dark backgrounds.

## Typography

This design system utilizes **Inter** for its systematic clarity and neutral, tech-forward appearance. 

- **Display sizes** use heavy weights and tight tracking to mirror the impact of architectural monoliths.
- **Body text** maintains generous line height to ensure readability against complex blurred backgrounds.
- **Label styles** are often uppercase with increased letter spacing to emulate the technical readouts of a HUD (Heads-Up Display).

## Layout & Spacing

The layout follows a **Mobile-First, Fluid Grid** philosophy. On mobile devices, content is stacked vertically with narrow gutters to maximize the "window" into the VR world. On desktop, the layout expands to a 12-column grid with wide margins to create a cinematic widescreen effect.

**Scroll-Driven Behavior:** Elements should utilize `view-timeline` to fade in and scale up as they enter the viewport, simulating the emergence of objects from the deep sea or the void of space.

## Elevation & Depth

Depth is achieved through **optical layering** rather than traditional shadows:
- **Level 0 (Abyss):** The primary background (#021026), often containing a subtle radial gradient or a fixed background video of moving water/stars.
- **Level 1 (Submerged):** Large containers with a 10% opacity white fill and a 20px `backdrop-filter: blur()`.
- **Level 2 (Surface):** Interactive cards with a 20% opacity fill, a 1px border of #9fb8c8 at 30% opacity, and a "glow" shadow using the Primary color at very low opacity (5-10%).
- **Level 3 (HUD):** Floating elements like buttons or tooltips that use a "Cian Vibrante" outer glow to appear self-illuminated.

## Shapes

The design system uses a **Rounded** language (0.5rem base) to soften the technical edges, making the futuristic interface feel organic and approachable. 
- **Cards and Modals:** Use `rounded-lg` (1rem) to create a distinct, encapsulated feel.
- **3D Placeholders:** Should always be contained within rounded-rect frames to integrate with the UI.
- **Buttons:** Use a higher roundedness (2rem or pill-shaped) to distinguish them as primary touch targets.

## Components

### Buttons
Primary buttons feature a solid #00d4ff fill with a `drop-shadow` cian glow. Secondary buttons are "ghost" style with a thin #9fb8c8 border that pulses slightly on hover.

### Glassmorphic Cards
These are the core of the experience. They must have `backdrop-filter: blur(16px)` and a linear gradient border (from top-left #9fb8c8 to bottom-right transparent) to simulate light hitting the edge of a glass pane.

### Media Placeholders (Video/3D)
Represented by containers with a 5% primary color tint and a pulsing play/interact icon. 3D models should have a "ground shadow" that is actually a blurred cian ellipse to represent a holographic projection base.

### Form Inputs
Minimalist underlines or very subtle dark-filled boxes. Focus states trigger a vertical cian "light bar" on the left edge of the input.

### Navigation
A bottom-docked "HUD" bar on mobile, utilizing high-blur glassmorphism and haptic-responsive icons. On desktop, a floating top-bar that disappears on scroll down and reappears on scroll up.