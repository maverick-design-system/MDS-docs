
# Images & Avatar 

The **Images & Avatar System** ensures visual consistency, scalability, and accessibility for all media components across your interface. It defines rules for aspect ratio, sizing, shape, and responsive behavior promoting a cohesive user experience on desktop, tablet, and mobile.


## Images

Images are used to represent visual content like **banners, media cards, thumbnails, and hero sections**. Their styling and layout are governed by fixed aspect ratios and corner radii defined in the Design System.

### Image Aspect Ratios

| Image Type   | Aspect Ratio | Desktop         | Tablet         | Mobile         |
|--------------|--------------|------------------|----------------|----------------|
| **Thumbnail** | 16:9         | 320×180 px       | 240×135 px     | 160×90 px      |
| **Media Card**| 4:3          | 360×270 px       | 200×150 px     | 160×120 px     |
| **Hero Image**| 16:9         | 1280×720 px      | 960×540 px     | 640×360 px     |
| **Banner**    | 3:1          | 1280×400 px      | 960×320 px     | 600×200 px     |

### Image Guidelines

- Use consistent **aspect ratios** to ensure layout stability across breakpoints.
- Apply the system-defined **corner radius** (usually 8px or `A spacing` token) to maintain a consistent visual tone.
- Avoid placing important text inside images — use text overlays with real HTML or component-level typography for accessibility.
- Images should **never stretch or skew** — maintain aspect ratio.
- Optimize all image assets for web performance (lazy loading, compression, responsive sets).
- Ensure **alt text** is descriptive and accessible.
- Use **responsive sets** to provide high-quality images for all screen sizes.
- Images should adapt **fluidly**:
  - **Mobile:** Vertical stacking prioritized
  - **Tablet & Desktop:** Horizontal layout benefits visual hierarchy


## Avatars

Avatars are visual representations of **users, teams, or entities** and serve as key identity anchors throughout the UI. They support:
- User profile photos
- Initials fallback (e.g., “MG”)
- Default system icons when no data is available

Avatars are **always circular** and maintain a **1:1 aspect ratio** to ensure symmetry and consistency.

### Avatar Size Variants

| Size   | Desktop        | Tablet         | Mobile         | Use Case                       |
|--------|----------------|----------------|----------------|--------------------------------|
| **Small**  | 32×32 px         | 28×28 px         | 24×24 px         | Message lists, chats, table rows |
| **Medium** | 48×48 px         | 40×40 px         | 36×36 px         | Comment cards, side nav, settings |
| **Large**  | 64×64 px         | 56×56 px         | 48×48 px         | Headers, user preview areas      |
| **Max**    | 200×200 px       | 160×160 px       | 128×128 px       | Profile screens, onboarding views |

### Border Radius

- **Radius:** `999px` (fully circular)
- Applied uniformly across all sizes
- Must remain consistent even for avatars with image, initials, or icon fallback

### Avatar Guidelines

- Use **initials** fallback (first name + last name initials) when no image is available.
- All avatars must have an accessible **alt text** or `aria-label`.
- Combine with visual states:
  - Online indicators (e.g., green dot)
  - Verified status (e.g., checkmark badge)
  - Camera or edit icon overlays for profile settings

### Avatar Component Principles

- **Base Avatar** is the foundational UI component. It is scalable, responsive, and adaptable across sizes and content types.
- Must support:
  - **Image**: user-uploaded photo
  - **Initials**: auto-generated
  - **Icon**: fallback for anonymous users
- Variant props include:
  - Shape (default = circular)
  - Size (small → max)
  - Presence states (online, away, offline)
  - Interaction state (clickable, editable)


## Images & Avatars in Action

Use imagery and identity visuals to guide attention and improve personalization. Below are some practical component applications and how they leverage the system:

| Component         | Image Type   | Avatar Size | Elevation Layer | Notes                              |
|------------------|--------------|-------------|------------------|-------------------------------------|
| Media Card        | 4:3 Image    | Small       | Low Elevation    | Product previews, articles          |
| Chat List Item    | N/A          | Small       | None             | User presence, initials fallback    |
| Profile Summary   | N/A          | Max         | Mid Elevation    | Prominent identity info             |
| Header Section    | Hero Image   | Medium      | High Elevation   | Background visual + user info       |
| Modal or Dialog   | N/A          | Medium      | Overlay + Scrim  | Uses Avatar + interactive states    |



## Best Practices

- Always maintain image aspect ratios — do not stretch or skew.
- Use system-defined sizes and avoid ad-hoc pixel values.
- Ensure avatars degrade gracefully with fallbacks.
- Never crop avatars to a non-circular shape unless explicitly styled for a group.
- Include alt text for images and aria-labels for avatars for screen reader compatibility.
- Optimize images for web performance (lazy loading, compression, responsive sets).
- Use consistent spacing and alignment to maintain visual harmony.
- Leverage visual hierarchy to guide attention and improve user experience.
- Use images to convey information, not just aesthetics.
- Avoid using images as decorative elements unless they add significant value.
- Ensure images are accessible to all users, including those with visual impairments.
- Use images to
  - Provide context and clarity
  - Enhance user experience
  - Improve brand recognition
  - Increase engagement
  - Increase conversions
  - Increase revenue
  - Increase retention
  - Increase customer satisfaction
  - Increase customer loyalty
  - Increase customer advocacy
  - Increase customer retention
  - Increase customer lifetime value


## 🧪 Developer Tip

Define image and avatar tokens like so:

```css
:root {
  --avatar-radius: 999px;
  --avatar-size-sm: 32px;
  --avatar-size-md: 48px;
  --avatar-size-lg: 64px;
  --avatar-size-max: 200px;

  --image-ratio-16-9: aspect-ratio: 16 / 9;
  --image-ratio-4-3: aspect-ratio: 4 / 3;
  --image-radius: 8px;
}
