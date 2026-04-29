# Design System Strategy: The Editorial Sanctuary

This design system is a departure from the rigid, grid-locked structures of traditional corporate web design. For a home staging professional, our digital environment must mirror the physical one: it must feel curated, spacious, and intentionally layered. We are moving away from "interfaces" and toward "interiors."

## 1. Overview & Creative North Star: "The Digital Curator"
The Creative North Star for this system is **The Digital Curator**. Unlike a standard service site, this system treats every screen like a high-end interior design spread. We prioritize white space, asymmetrical layouts, and "breathable" components. 

To break the "template" look, we utilize **Intentional Asymmetry**. For example, a hero section shouldn't just be a centered box; it should feature overlapping elements—a large image slightly offset by a floating, soft-edged text container—to mimic the layered textures of a well-staged home.

## 2. Colors & Surface Philosophy
The palette is rooted in organic warmth. We use `surface` (#fcf9f4) as our primary canvas, avoiding the sterile coldness of pure white (#ffffff) or harsh grays.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to section content. Traditional dividers create visual "noise" that contradicts an empathetic, calm vibe. 
- **Boundaries:** Define sections solely through background shifts. Transition from `surface` to `surface-container-low` (#f6f3ee) to signal a new content block.
- **Nesting:** To create focus, nest a `surface-container-lowest` (#ffffff) card inside a `surface-container` (#f0ede8) section. This creates "natural" depth without artificial lines.

### Signature Textures & Gradients
Flat color can feel clinical. To inject "soul," use subtle linear gradients for primary actions or headers:
- **Warmth Gradient:** A transition from `primary` (#9a402a) to `primary-container` (#b95840) at a 135-degree angle. This provides a tactile, "sun-drenched" quality to buttons and hero backgrounds.

## 3. Typography: The Modern Editorial
We utilize two distinct sans-serifs to create a hierarchy that feels both professional and personal.

*   **The Display Voice (Plus Jakarta Sans):** Used for `display` and `headline` scales. This font’s open counters and modern geometry feel "expensive" yet approachable. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create an authoritative, editorial impact.
*   **The Functional Voice (Be Vietnam Pro):** Used for `title`, `body`, and `label` scales. It is exceptionally legible at small sizes, maintaining the "Caring Consultant" persona through its soft, rhythmic curves.

**Hierarchy Tip:** Pair a `display-md` headline in `on-surface` (#1c1c19) with a `title-md` subheader in `tertiary` (#745541) to create a sophisticated, multi-tonal typographic hierarchy.

## 4. Elevation & Depth: Tonal Layering
In this system, depth is a feeling, not a drop-shadow.

*   **The Layering Principle:** Stack surfaces like fine paper. 
    - Base: `surface`
    - Section: `surface-container-low`
    - Card: `surface-container-lowest` (this creates a subtle, "lifted" effect).
*   **Ambient Shadows:** If an element must float (like a navigation bar), use an extra-diffused shadow: `box-shadow: 0 12px 40px rgba(137, 114, 109, 0.08)`. Notice we use a tinted version of `outline` (#89726d) for the shadow color rather than black, keeping the look organic.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline-variant` (#dcc0ba) at 20% opacity. It should be felt, not seen.
*   **Glassmorphism:** For overlays or sticky headers, use `surface-container-lowest` at 80% opacity with a `backdrop-blur: 12px`. This allows the warm room photography to bleed through, maintaining a sense of place.

## 5. Components

### Buttons
- **Primary:** `primary` (#9a402a) background with `on-primary` (#ffffff) text. Use `rounded-xl` (3rem) for a pill-like, soft appearance. 
- **Secondary:** `secondary-container` (#acebeb) with `on-secondary-container` (#2c6c6c). This provides a gentle contrast to the terracotta primary.
- **Interaction:** On hover, shift background to the `primary-container` (#b95840) to simulate a "glow."

### Cards & Lists
- **The Container:** Always use `rounded-lg` (2rem) or `rounded-xl` (3rem). 
- **Anti-Divider Policy:** For lists, never use lines. Use `1.5rem` to `2rem` of vertical white space (gap) between items. Use a subtle `surface-container-high` (#ebe8e3) background on hover to indicate interactivity.

### Input Fields
- **Styling:** Use `surface-container-highest` (#e5e2dd) for the input background. 
- **Shape:** `rounded-md` (1.5rem) to ensure they feel soft enough to touch but structured enough to fill.
- **Focus State:** Instead of a thick border, use a 2px `outline` (#89726d) with a soft glow effect using the `surface-tint`.

### Signature Component: The "Consultant Quote"
A bespoke component for this system: A large-format card using `tertiary-fixed` (#ffdcc6) background, `display-sm` typography, and an asymmetrical image placement of the professional. This builds the "Caring Consultant" trust.

## 6. Do’s and Don’ts

| Do | Don't |
| :--- | :--- |
| **Do** use asymmetrical margins to create an editorial, high-end feel. | **Don't** use a standard 12-column bootstrap-style grid that feels "templated." |
| **Do** use `secondary` (#276868) for accents like icons to provide a "cool" relief to the warm palette. | **Don't** use pure black (#000000) for text. Use `on-surface` (#1c1c19) for better optical comfort. |
| **Do** utilize `rounded-xl` on all image containers to mirror the soft furniture edges of a staged home. | **Don't** use sharp corners or 0px border radius; it feels aggressive and corporate. |
| **Do** rely on font-weight and color (e.g., `tertiary`) to create hierarchy. | **Don't** use 1px lines or dividers to separate content blocks. |