# NK Bag House — Design System Foundation

This document defines the reusable UI rules for the frontend. It is a starting specification, not a final brand identity. Exact colours, typefaces, and imagery should be approved against the customer's logo and visual references before implementation.

## 1. Design principles

- **Clear hierarchy:** every page should have one primary heading and a clear next action.
- **Consistency:** repeated components should look and behave the same.
- **Purposeful spacing:** use a predictable spacing scale rather than arbitrary margins.
- **Readable content:** prioritise legibility over decorative effects.
- **Authentic imagery:** use approved NK Bag House product and manufacturing photographs.
- **Accessible interaction:** keyboard, focus, contrast, and touch behaviour are part of the design.

## 2. Colour tokens

Use semantic tokens so the visual theme can be changed without rewriting components.

| Token | Purpose | Brand value |
|---|---|---|
| `--color-background` | Main page background | Pending approval |
| `--color-surface` | Cards and panels | Pending approval |
| `--color-text` | Main text | Pending approval |
| `--color-muted` | Secondary text | Pending approval |
| `--color-primary` | Main brand action | Pending approval |
| `--color-primary-contrast` | Text on primary action | Pending approval |
| `--color-border` | Dividers and outlines | Pending approval |
| `--color-success` | Successful feedback | Accessible semantic value |
| `--color-danger` | Error feedback | Accessible semantic value |

A restrained neutral base with one recognisable brand accent is a useful starting direction. Do not lock a final palette until the logo and customer references have been reviewed. Check text and interactive contrast rather than relying on colour appearance alone.

## 3. Typography

Use a small, deliberate type system:

- Display: homepage hero and major editorial statements.
- Heading 1: page title.
- Heading 2: major section title.
- Heading 3: card or subsection title.
- Body: descriptions and explanatory text.
- Small: metadata, labels, and supporting information.

Use no more than two complementary font families unless the brand already has a defined typeface. Prefer a highly readable body face. Use fluid sizing carefully and keep line lengths comfortable.

## 4. Spacing and layout

Use a consistent spacing scale (for example, 4, 8, 12, 16, 24, 32, 48, 64, and 80 CSS pixels). Choose values from the scale rather than inventing a new value for every component.

- Establish a shared page container and content max-width.
- Align section headings, grids, and calls to action to a consistent layout grid.
- Use larger vertical spacing between major sections than between related elements.
- Avoid both crowded cards and excessively tall empty sections.
- Ensure layouts do not cause horizontal scrolling at supported viewport widths.

## 5. Component standards

### Buttons

- Primary: one dominant action, normally "Request a Quote" or "Send Enquiry".
- Secondary: navigation to supporting content, such as "Explore Products".
- Text link: low-emphasis navigation.
- Provide default, hover, focus-visible, active, disabled, and loading states.
- Use clear action labels; avoid vague labels such as "Click here".

### Product cards

- Consistent image ratio and crop behaviour.
- Product name and factual short descriptor.
- Optional category label when useful.
- One clear action.
- Entire card should not become an ambiguous nested collection of links and buttons.

### Forms

- Visible labels, appropriate input types, and clear required-field indicators.
- Helpful instructions and specific inline errors.
- Preserve entered values after validation errors.
- Keyboard-operable controls and visible focus.
- Success and failure states that are announced accessibly.

### Navigation

- Clearly identify the current page.
- Support keyboard operation and mobile navigation.
- Avoid hover-only menus.
- Keep the quote action visible without making the header crowded.

## 6. Imagery

- Use actual, approved product and manufacturing images.
- Keep image ratios consistent within the same component family.
- Define focal points so important parts of a bag or product are not cropped out.
- Use optimised responsive image sizes.
- Provide meaningful alt text for informative images; use empty alt text for purely decorative images.
- Do not use competitor logos, screenshots, product photography, or marketing copy as NK Bag House assets.

## 7. Motion

- Use short transitions for hover, focus, and menu state changes.
- Avoid parallax, auto-advancing carousels, and large entrance animations unless there is a clear user benefit.
- Respect reduced-motion preferences.
- Never make important content available only through animation.

## 8. Responsive layout checkpoints

Test at a narrow mobile width, a typical mobile width, tablet, laptop, and wide desktop. Exact breakpoints should follow the content and Tailwind configuration rather than being treated as fixed brand rules.

Check:
- Header and navigation wrapping.
- Product grid column changes.
- Image focal points.
- Form field widths and error messages.
- Tables and long specification labels.
- Footer stacking and contact actions.

## 9. Implementation rule

Build shared components only after identifying repeated patterns. Keep tokens centralised (for example, CSS variables in the global stylesheet) and avoid duplicating arbitrary colour, spacing, or radius values across page files.

## 10. Approval status

The component principles are ready for use. Final colour values, fonts, logo treatment, imagery style, and exact responsive breakpoints remain pending customer reference review.
