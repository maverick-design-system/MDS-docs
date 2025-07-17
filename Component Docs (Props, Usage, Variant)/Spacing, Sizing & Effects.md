

# Spacing, Sizing & Effects

Consistency in spacing, sizing, and effects is essential to maintain **clarity, rhythm, and usability** across components and layouts. Our system is built on a **4pt baseline grid**, applied to padding, margins, gaps, radii, and visual feedback elements.


## Spacing Scale

The spacing system defines semantic tokens (e.g., `space-sm`, `space-lg`) mapped to pixel values. These tokens help maintain rhythm and eliminate arbitrary values across the UI.

| Token       | Value  | Use Case Examples |
|-------------|--------|-------------------|
| `space-0`   | 0px    | No spacing / reset |
| `space-xxs` | 4px    | Icon spacing, tiny gaps |
| `space-xs`  | 8px    | Button padding, checkbox gap |
| `space-sm`  | 12px   | Inline labels, micro gaps |
| `space-md`  | 16px   | Base padding, list items |
| `space-lg`  | 20px   | Cards, containers |
| `space-xl`  | 24px   | Section padding, grid gutters |
| `space-2xl` | 28px   | In-between content sections |
| `space-3xl` | 32px   | Modal padding, layout spacing |
| `space-4xl` | 36px   | Headers to block elements |
| `space-5xl` | 40px   | CTA separation, blocks |
| `space-6xl` | 48px   | Page sections, large components |
| `space-7xl` | 64px   | Section to section spacing |
| `space-8xl` | 80px   | Hero paddings |
| `space-9xl` | 96px   | Landing page vertical rhythm |
| `space-10xl`| 128px  | Desktop white space |
| `space-11xl`| 160px  | Full-screen sections |
| `space-12xl`| 192px  | Enterprise-scale vertical spacing |


## Grid System

A grid system ensures alignment, scalability, and rhythm across responsive layouts. Ours is based on 4, 6, 8, or 12-column layouts depending on the device width.

### Grid Structure

| Screen Size             | Columns | Margin     | Gutter     | Use Case                             |
|-------------------------|---------|------------|------------|--------------------------------------|
| Mobile (320px–599px)    | 4       | 16px       | 12px       | Simple stacking, compact layouts     |
| Tablet (600px–1135px)   | 6       | 32px       | 20px       | Sidebars, cards, media grids         |
| Desktop (1136px+)       | 12      | 112px      | 32px       | Full dashboard/web app layouts       |
| Fluid Containers        | Auto    | 24px       | 24px       | Cards, modals, reusable sections     |

### 🧭 Grid Terms

- **Columns:** Vertical content blocks
- **Gutters:** Space between columns
- **Margins:** Space on outer edges of the grid
- **Container:** Max-width wrapper that holds the grid

### Do
- Use **4 or 6 columns** for mobile
- Maintain **gutters** for spacing clarity
- Use **fluid containers** for modular sections
- Use **margins** for layout spacing
- Use **112px** margin for desktop layouts
- Use **16px** margin for mobile layouts

### Don’t
- Skip gutters or uneven spacing
- Override margins arbitrarily across breakpoints

## Border Radius System

Corner radii provide consistency and personality to UI components. A smooth, scalable radius system helps distinguish surfaces while maintaining cohesion.

| Token         | Radius   | Use Cases                        |
|---------------|----------|----------------------------------|
| `radius.0`    | 0px      | Sharp edges (tables, dividers)   |
| `radius.sm`   | 4px      | Tags, badges                     |
| `radius.md`   | 8px      | Inputs, cards, modals            |
| `radius.lg`   | 12px     | Large cards, overlays            |
| `radius.xl`   | 16px     | Hero sections, app shells        |
| `radius.full` | 999px    | Circular buttons, avatars        |


##  Visual Effects

Visual effects like shadows and overlays enhance **depth, feedback, and focus**. These are applied via predefined tokens for clarity and consistency.

### Shadow Tokens

| Token        | X   | Y   | Blur | Spread | Opacity | Use Case                           |
|--------------|-----|-----|------|--------|---------|------------------------------------|
| `shadow-low` | 0px | 2px | 2px  | 0px    | 15%     | Cards, inputs                      |
| `shadow-mid` | 0px | 4px | 4px  | 0px    | 20%     | Dropdowns, menus, buttons          |
| `shadow-high`| 0px | 6px | 8px  | 0px    | 20%     | Tooltips, banners, snackbars       |

Use subtle shadows for clarity, avoid harsh or stacked shadows.

###  Scrim Layer (Overlay)

Scrims are used behind dialogs, modals, or overlays to create visual separation and focus.

- **Color:** `#000000`
- **Opacity:** `25%`
- **Use Cases:** Modals, bottom sheets, popovers

```css
.modal-overlay {
  background-color: rgba(0, 0, 0, 0.25);
}
````

 ### Summary
Design Token	Category	Description
1. **space**	Spacing	Padding, margin, gaps
2. **radius**	Border Radius	Visual roundness of corners
3. **shadow**	Elevation	Visual depth using drop shadows
4. **scrim-overlay**	Effect	Background for modal overlays

This system ensures visual cohesion, device adaptability, and scalable UI patterns across your product.


## Developer Example

```css
:root {
  --space-md: 16px;
  --radius-md: 8px;
  --shadow-low: 0px 2px 2px rgba(0, 0, 0, 0.15);
  --scrim-overlay: rgba(0, 0, 0, 0.25);
}
.card {
  padding: var(--space-md);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-low);
} 
```

