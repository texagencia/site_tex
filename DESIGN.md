# High-End Real Estate Growth: Design System Manual

## 1. Overview & Creative North Star: "The Architectural Monolith"
This design system is built upon the concept of **"The Architectural Monolith."** Like a luxury penthouse or a brutalist masterpiece, the interface must feel structural, permanent, and expensive. We move away from the "bubbly" consumer web and toward a high-ticket, editorial experience.

**The Creative North Star** dictates that every pixel must serve a purpose. We achieve prestige through **intentional asymmetry**, where large headings are offset against vast "white space" (Deep Black), and **tonal depth**, where layers are defined by light and shadow rather than lines. We are not building a website; we are curate a digital gallery of high-value opportunities.

---

## 2. Colors & Surface Philosophy

The palette is rooted in high-contrast prestige. We use `surface` tokens to create a sense of physical material.

### The "No-Line" Rule
**Prohibit 1px solid borders for sectioning.** To define boundaries between content blocks, use background color shifts. A `surface-container-low` section should sit directly against a `surface` background. If you feel the need to draw a line, use a margin instead.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked architectural materials.
*   **Base:** `surface` (#131313) for the main canvas.
*   **Sunken:** `surface-container-lowest` (#0e0e0e) for footer areas or utility trays.
*   **Elevated:** `surface-container` (#1f1f1f) for primary content cards.
*   **Floating:** `surface-bright` (#393939) for active navigation or high-priority modals.

### The "Glass & Gold" Rule
*   **Glassmorphism:** For floating navigation or over-image overlays, use `surface-variant` at 40% opacity with a `20px` backdrop-blur. This simulates frosted obsidian.
*   **Signature Textures:** Never use a flat `primary` (#f2ca50) for large areas. Apply a subtle linear gradient (135deg) from `primary` to `primary_container` (#d4af37) to mimic the way light hits real metallic gold.

---

## 3. Typography: The Editorial Voice

We pair the technical precision of **Space Grotesk** with the humanistic clarity of **Manrope**.

*   **Display & Headlines (Space Grotesk):** These are your "Architectural Anchors." Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create a commanding presence. Headlines should often be "Primary" gold or "Pure White" to contrast against the dark void.
*   **Body & Titles (Manrope):** Manrope provides the "Consultant’s Voice"—professional and trustworthy. Use `body-lg` (1rem) for long-form insights.
*   **The Power of Scale:** Create drama by placing a `label-sm` (all-caps, tracked out 0.1em) immediately above a `display-md` headline. This "Label-to-Display" jump is a hallmark of premium editorial design.

---

## 4. Elevation & Depth: Tonal Layering

We do not use shadows to mimic light; we use tonal layering to mimic material.

*   **The Layering Principle:** Depth is achieved by "stacking" the surface-container tiers. Place a `surface-container-high` (#2a2a2a) element inside a `surface-container-low` (#1b1b1b) wrapper to create a soft, natural lift.
*   **Ambient Shadows:** If a floating element (like a CTA modal) requires a shadow, it must be invisible to the untrained eye. Use a 40px blur, 0% spread, and `on-background` at 8% opacity.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline-variant` token at 15% opacity. **Never use 100% opaque borders.**

---

## 5. Components & Primitive Styling

### Buttons: The Signature CTA
*   **Primary:** A gradient from `primary` to `primary_container`. Text: `on_primary` (Deep Black). Shape: Sharp `0px` corners. No exceptions.
*   **Secondary:** `surface-container-highest` background with a `primary` text color.
*   **Interaction:** On hover, the gold gradient should shift 45 degrees, creating a "shimmer" effect.

### Cards: The Content Blocks
*   **Structure:** No dividers. Use `Spacing 8` (2.75rem) to separate internal card elements.
*   **Background:** Use `surface-container-low` (#1b1b1b).
*   **Hover:** Transition the background to `surface-container-high` (#2a2a2a) and add a "Ghost Border" of `primary` at 20% opacity.

### Input Fields: The Professional Inquiry
*   **Style:** Underline-only or flat `surface-container-highest` fills.
*   **Active State:** The bottom border transforms into a `primary` (Gold) 2px line.
*   **Error:** Use `error` (#ffb4ab) typography, but keep the container dark to maintain the premium feel.

### Specialized Component: The Property Metric
For a real estate growth agency, we need a "Metric Hero." This is a large `display-lg` number in `primary` gold, with a `label-md` description underneath in `on-surface-variant` (muted tan). No boxes, no borders—just raw data as art.

---

## 6. Do’s and Don’ts

### Do
*   **DO** use extreme vertical spacing. Use `Spacing 24` (8.5rem) between major sections to let the design breathe.
*   **DO** use "Pure White" (#FFFFFF) sparingly—only for the most critical body text or highlights.
*   **DO** ensure all interactive elements have sharp `0px` corners to reinforce the "Architectural" feel.

### Don’t
*   **DON'T** use rounded corners. This system is built on 90-degree precision.
*   **DON'T** use standard grey shadows. Shadows should feel like ambient occlusion in a dark room.
*   **DON'T** use icons unless they are ultra-thin, stroke-based, and perfectly aligned to a 24px grid.
*   **DON'T** use "divider lines" to separate list items. Use a subtle background shift on every second item or simply increase the `Spacing` scale.