
## Iconography

### Overview

Iconography plays a vital role in user interface design by providing visual cues, enhancing recognition, and improving navigation. This system establishes consistent styling, weight options, and usage guidelines for all icons — both UI-specific and brand-related — ensuring visual harmony across the product.


### Icon Weights & Styles

Icons are available in multiple visual weights to suit various design needs:

| Weight      | Description                                                                 |
| ----------- | --------------------------------------------------------------------------- |
| **Thin**    | Minimal and elegant. Best for subtle UIs and lightweight design contexts.   |
| **Light**   | Slightly more pronounced than Thin, offering better legibility.             |
| **Regular** | The default icon weight — ideal for most UI elements and actions.           |
| **Bold**    | Highly visible and strong. Use for emphasis or primary interaction points.  |
| **Fill**    | Solid icons without outlines. Great for compact spaces or dark backgrounds. |
| **Duo**     | Dual-tone icons with layered effects. Use sparingly for expressive content. |

> Tip: Pair icon weights with matching font weights and visual densities to maintain aesthetic balance.


### Outline vs Stroke

* **Outline Icons**: Use clean paths with transparent interiors. Best for modern, minimal designs.
* **Stroke Icons**: Feature consistent stroke width and open shapes. Ideal for scalable and editable components.

Both styles can be used depending on the context, but maintain consistency across similar UI clusters (e.g., form controls, navigation bars, tooltips).


### Icon Sizes & Grid

Icons are built on a consistent vector grid (typically 24×24 px or 16×16 px) to ensure visual alignment and pixel precision.

| Size   | Use Case                          |
| ------ | --------------------------------- |
| 16 px  | Toolbars, menus, tags             |
| 20 px  | Buttons, inputs                   |
| 24 px  | Primary navigation, tabs          |
| 32+ px | Hero icons, empty states, banners |

Maintain optical balance when placing icons near text or UI components. Use spacing tokens for padding and gaps between icon and label.


### Brand Icons

The system includes a library of brand icons (e.g., Google, Apple, GitHub, Twitter, Discord, etc.) available in the same weights and styles as UI icons.

> Use brand icons respectfully and according to their platform’s brand usage guidelines.

---

### Best Practices

**Do:**

* Maintain a consistent weight/style within the same interface.
* Align icons to the pixel grid to avoid blur.
* Pair icons with tooltips or labels for clarity.
* Use icons to enhance, not replace, text (especially for accessibility).

**Don’t:**

* Mix weights and styles haphazardly.
* Use icons out of brand context (e.g., altered brand logos).
* Overload the interface with too many icons.
* Use decorative icons without functional meaning.


### Accessibility Consideration

All icons must have accessible labels (`aria-label`, `title`, or alternative text). Avoid using icons as the sole means of conveying meaning. Always provide text support for critical actions.


