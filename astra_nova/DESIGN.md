```markdown
# Design System Documentation: Aerospace & Orbital Retail

## 1. Overview & Creative North Star
**Creative North Star: The Celestial Navigator**
This design system is not a standard e-commerce template; it is a high-precision flight interface. We are moving away from the "flat web" to create an experience that feels like a premium Head-Up Display (HUD) integrated into a luxury spacecraft. 

The aesthetic is driven by **Atmospheric Engineering**: the tension between the vast, dark void of space and the razor-sharp precision of aerospace technology. We break the rigid, predictable grid through intentional asymmetry—using large-scale typography that bleeds off-canvas and overlapping glass containers that mimic the complex layering of cockpit instrumentation. The goal is to make the user feel like they are not just "browsing," but "commanding."

---

## 2. Colors & Tonal Depth
Our palette is rooted in the deep spectrum of the cosmos, using light not just as decoration, but as data.

*   **Primary (Photon Blue - #98cbff):** Represents energy and propulsion. Use this for active states and primary brand moments.
*   **Surface (Deep Space - #121318):** The infinite void. This is our canvas.
*   **Tertiary (Emergency Orange - #ffb59a):** Reserved strictly for critical actions (CTAs), mission-critical alerts, and "Launch" triggers.
*   **Secondary (Metallic Silver - #c6c6c6):** Used for technical hardware specs and secondary UI elements to provide a machined, industrial feel.

### The "No-Line" Rule
Standard 1px borders are prohibited for sectioning. They feel "web-like" and fragile. Boundaries must be defined solely through **Background Tonal Shifts**. For example, a section using `surface-container-low` should sit directly against the `surface` background. The eye should perceive the change in depth through color value, not an artificial line.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers.
*   **Level 0 (The Void):** `surface` (#121318) for the main background.
*   **Level 1 (The Bulkhead):** `surface-container-low` (#1a1b21) for large content areas.
*   **Level 2 (The Console):** `surface-container-high` (#292a2f) for interactive cards.
*   **Level 3 (The Interface):** `surface-container-highest` (#34343a) for floating elements.

### The "Glass & Gradient" Rule
To move beyond a flat interface, use **Glassmorphism** for floating modules. Apply `surface-variant` at 40% opacity with a `backdrop-blur` of 20px. Enhance this with a subtle linear gradient transitioning from `primary` to `primary-container` (at 10% opacity) to give the glass a "charged" feel.

---

## 3. Typography
We use typography to balance "Visionary Ambition" with "Technical Reliability."

*   **Display & Headlines (Space Grotesk):** This is our "wide" sans-serif. It feels expansive and modern. Use `display-lg` (3.5rem) with `-0.02em` letter spacing for hero sections to create a commanding presence.
*   **Body & Technical Specs (Manrope):** Our workhorse. It provides the legibility of a monospaced font without the "hacker" cliché. Use `body-md` (0.875rem) for all technical descriptions.
*   **Labels (Space Grotesk):** Use `label-sm` (0.6875rem) in all-caps with `0.1rem` letter spacing for metadata (e.g., "THRUST CAPACITY," "ORBITAL RADIUS"). This mimics engineering schematics.

---

## 4. Elevation & Depth
Depth in this system is a simulation of light reflecting off high-end materials.

### The Layering Principle
Achieve lift by stacking containers. A `surface-container-lowest` card placed on a `surface-container-low` section creates a recessed, "machined" look. Conversely, a `surface-container-highest` element creates a "raised" effect.

### Ambient Shadows
Shadows should be nearly invisible. When a floating state is required, use a blur of `40px` with the color `surface-container-lowest` at 50% opacity. This creates a "glow" rather than a "shadow," suggesting the element is emitting light.

### The "Ghost Border" Fallback
If a visual separator is mandatory for accessibility, use a **Ghost Border**: the `outline-variant` token (#3f4852) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary (Launch):** Background: `tertiary-container` (#ff7134). Shape: `sm` (0.125rem) for sharp, aggressive corners. Use a subtle outer glow of `tertiary` at 20% opacity.
*   **Secondary (Navigation):** Background: Transparent with a Ghost Border. Text: `primary`. On hover, transition to `surface-bright` with a `0.5rem` horizontal slide animation.

### Cards & Tech Specs
*   **Rule:** Forbid the use of divider lines.
*   **Structure:** Use `spacing-8` (2.75rem) to separate content blocks. Group technical data using `surface-container-highest` backgrounds with `sm` roundedness. 
*   **Visuals:** Always pair cards with high-fidelity spacecraft imagery. Use an inner-shadow (inset) to make images feel like they are behind a glass porthole.

### Input Fields
*   **Style:** Underline only. Use `outline` (#88919d) for the default state. Upon focus, the line transforms to `primary` (#98cbff) with a subtle "flicker" animation (0.1s) to simulate a system powering on.

### Interaction Chips
*   **Selection:** Use `secondary-container` (#484949) with `full` roundedness. When selected, apply a 2px `surface-tint` outer glow.

---

## 6. Do’s and Don’ts

### Do:
*   **Use Intentional Asymmetry:** Offset your text blocks. If a spacecraft image is aligned right, let the headline overlap it slightly to create depth.
*   **Embrace Negative Space:** Space is vast. Use `spacing-24` (8.5rem) between major sections to let the "premium" feel breathe.
*   **Mix Edges:** Use `none` or `sm` roundedness for structural containers, but `full` for interactive "pills" to mimic aerodynamic curves.

### Don’t:
*   **No "Flat" Buttons:** Never use a flat, 2D color without a slight tonal gradient or glass effect. It breaks the "high-tech hardware" illusion.
*   **No High-Contrast Borders:** Avoid 100% opaque `outline` tokens. They create visual noise that distracts from the spacecraft imagery.
*   **No Generic Grids:** Avoid the "3-column card row" where possible. Try a 2/3 and 1/3 split to create a more editorial, sophisticated layout.
*   **No Pure White:** Never use #FFFFFF. Use `on-surface` (#e3e1e9) to maintain the "low-light cockpit" atmosphere.

---
*Director's Note: Every pixel should feel like it was machined in a clean room. Precision is our primary brand value. If it feels like a "website," you haven't pushed the atmospheric depth far enough.*```