

# Elevation System
The **Elevation System** communicates the visual hierarchy and perceived depth of UI elements through subtle, consistent shadows. Elevation gives users visual cues about **interactivity**, **layering**, and **focus**, helping them navigate the interface more intuitively.

Each elevation level is defined by a set of shadow properties (x/y offset, blur, spread, and color opacity), optimized for accessibility across themes and devices.



## Elevation Levels

### Low Elevation

**Use Case:**  
Used for foundational containers such as cards, input fields, and surface sections.

**Effect Properties:**
- **X-axis:** `0px`  
- **Y-axis:** `2px`  
- **Blur:** `2px`  
- **Spread:** `0px`  
- **Color:** `#000000`  
- **Opacity:** `15%`

This level creates gentle separation between UI elements and the background without drawing too much attention. Common in layouts with dense content.



### Mid Elevation

**Use Case:**  
Used to indicate interactivity—particularly hover states and active feedback. Applies to components like:
- Dropdown menus  
- Elevated buttons  
- Chips  
- Menus

**Effect Properties:**
- **X-axis:** `0px`  
- **Y-axis:** `4px`  
- **Blur:** `4px`  
- **Spread:** `0px`  
- **Color:** `#000000`  
- **Opacity:** `20%`

This level signals to users that the component is elevated due to interaction (e.g., hover or focus) and may perform an action.

### High Elevation

**Use Case:**  
Used for overlay content that partially obscures the interface, such as:
- Tooltips  
- Snackbars  
- Banners  
- Sticky headers

**Effect Properties:**
- **X-axis:** `0px`  
- **Y-axis:** `6px`  
- **Blur:** `8px`  
- **Spread:** `0px`  
- **Color:** `#000000`  
- **Opacity:** `20%`

High elevation ensures overlays stand out prominently, signaling importance or urgency while maintaining accessibility and visual balance.



## Scrim Layer (Overlay Backdrop)

**Use Case:**  
Scrims are **semi-transparent backgrounds** used behind elevated elements such as modals, dialogs, and bottom sheets. They help:
- Dim the background to reduce visual clutter  
- Focus user attention on the elevated content  
- Prevent interaction with the obscured interface

**Visual Properties:**
- **Color:** `#000000`
- **Opacity:** `25%`
- **Type:** Solid fill

Although scrims do not cast shadows themselves, they are an essential part of the elevation system and should be included in any layered UI implementation.

## Elevations in Action

### Examples of Practical Usage:
| Component        | Elevation Tier | Notes |
|------------------|----------------|-------|
| **Card**         | Low Elevation  | Base layout structure |
| **Button (Hover)** | Mid Elevation  | Indicates interactivity |
| **Dropdown Menu**| Mid Elevation  | Active surface above base layer |
| **Snackbar / Tooltip** | High Elevation | Interruptive or urgent message |
| **Modal + Scrim**| High Elevation (with overlay) | Blocks background interaction |


## Best Practices

- Use **low elevation** for layout and content blocks.
- Use **mid elevation** for hover or focus states to guide interaction.
- Use **high elevation** for overlays and elements requiring immediate attention.
- Always pair **elevation** with **motion and color** for richer interaction feedback.
- Avoid stacking too many elevation layers unnecessarily—this causes visual noise.
- Ensure **contrast** between elevated elements and their background.
- Use **motion** to guide users through the interface, especially when changing elevation levels.
- **Accessibility:** Ensure that high elevation elements are still legible and usable with color contrast and font size.
- **Responsive Design:** Elevation should adjust appropriately for different screen sizes and orientations.
- **Consistency:** Maintain a consistent elevation system across all screens and components.


## Developer Tip

Use elevation as part of your design tokens or utility classes:

```css
:root {
  --elevation-low: 0px 2px 2px rgba(0, 0, 0, 0.15);
  --elevation-mid: 0px 4px 4px rgba(0, 0, 0, 0.2);
  --elevation-high: 0px 6px 8px rgba(0, 0, 0, 0.2);
  --scrim-overlay: rgba(0, 0, 0, 0.25);
}
```