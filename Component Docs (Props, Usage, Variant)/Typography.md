# Typography System

Typography is foundational to visual hierarchy, user experience, and brand identity. Our system is designed with **Poppins**, a clean, modern, geometric sans-serif font that brings clarity and structure to content across all platforms.

## Font Family

- **Primary Font:** Poppins
- **Font Weights Used:**  
  - Regular (400): Default for most text  
  - Medium (500): Used for emphasis or interactive elements like buttons

## Text Styles

| Style             | Font Size | Line Height | Weight | Letter Spacing | Use Case |
|------------------|-----------|-------------|--------|----------------|----------|
| **Display Large** | 56px / 3.5rem | 64px / 4rem | 400 / 500 | 0px | For hero sections, splash headers, and bold introductory statements. It creates immediate visual impact. |
| **Display Medium** | 45px / 2.8125rem | 52px / 3.25rem | 400 / 500 | 0px | For bold headlines on landing pages or key brand messages with slightly less visual weight than Display Large. |
| **Display Small** | 36px / 2.25rem | 44px / 2.75rem | 400 / 500 | 0px | Used for attention-grabbing text in feature banners, marketing blocks, or announcements. |
| **Headline Large** | 32px / 2rem | 40px / 2.5rem | 400 / 500 | 0px | Ideal for page titles on dashboards or content pages where a strong heading is needed. |
| **Headline Medium** | 28px / 1.75rem | 36px / 2.25rem | 400 / 500 | 0px | Used for major section headers inside a page. |
| **Headline Small** | 24px / 1.5rem | 32px / 2rem | 400 / 500 | 0px | Useful for subsections, card headers, or side panel titles. |
| **Title Large** | 22px / 1.375rem | 28px / 1.75rem | 400 / 500 | 0.4px | Used in dialog headers, large list titles, and app bars where space is limited but clarity is essential. |
| **Title Medium** | 20px / 1.25rem | 28px / 1.75rem | 400 / 500 | 0.5px | Great for reusable UI elements like modal titles, form section headers, or context headers. |
| **Title Small** | 18px / 1.25rem | 24px / 1.5rem | 400 / 500 | 0.15px | Used for card titles, grouped lists, or compact interface headings. |
| **Body Large** | 16px / 1rem | 24px / 1.5rem | 400 / 500 | 0.5px | The default for most text content, ideal for readable paragraphs, descriptions, and general UI copy. |
| **Body Medium** | 14px / 0.875rem | 20px / 1.25rem | 400 / 500 | 0.25px | Best used for supporting text, secondary content, descriptions below headings, or footnotes. |
| **Body Small** | 12px / 0.75rem | 16px / 1rem | 400 / 500 | 0.4px | For compact areas such as disclaimers, small notes, or inside elements like cards and inputs. |
| **Label Large** | 14px / 0.875rem | 20px / 1.25rem | 400 / 500 | 0.1px | For form labels above inputs, segmented controls, or tab labels. Clear and readable without being dominant. |
| **Label Medium** | 12px / 0.75rem | 16px / 1rem | 400 / 500 | 0.5px | Used in interactive elements like buttons, chips, or compact tags. |
| **Label Small** | 11px (optional) | 16px | 400 / 500 | -0.25px | For microcopy like helper text, hints, tooltips, or small inline labels. Should be used sparingly. |

##  Usage Guidelines

- **Consistency First:** Always use the predefined text styles rather than creating ad-hoc ones.
- **Accessibility:** Ensure sufficient contrast and readable font sizes (16px minimum for body).
- **Hierarchy:** Use typography weights and sizes to guide users' attention without overwhelming them.
- **Display Sizes:** Reserve large styles for impactful content don't use Display Large on every page.
- **Balance Font Weight:** Medium (500) should highlight important or interactive text like buttons or badges.



Each text type has a different function which is as follows:

| Text Style | Usage Example                          |
|------------|----------------------------------------|
| Display    |Hero headlines, landing pages intros,
|            |and branding                            |
| Headline   |            Headers                            |
| Title      |           Titles                             |
| Body       |                                        |
| Label      |                                        |

## Developer Tip

These styles can be implemented as CSS classes or design tokens. Example (using Tailwind-style naming for inspiration):

```css
.text-display-lg {
  font-size: 3.5rem;
  line-height: 4rem;
  font-weight: 400;
  letter-spacing: 0;
  font-family: 'Poppins', sans-serif;
}
```