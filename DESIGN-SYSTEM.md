# Portfolio design library

The shared styles in `styles.css` apply to the homepage and all project pages.

- Canvas: warm ivory `--paper` (#F7F7F2), used throughout, including placeholder artwork.
- Primary: forest green `--forest` (#214E3B); hover #173C2C. Text #243B30, secondary text #5C6C61. Soft green #E3EBE2 is reserved for small callouts.
- Typography: `--font-sans` (Segoe UI, Helvetica Neue, Arial) for headings and body; `--font-mono` for technical labels. Both use locally available fonts without downloads. Use the `--text-*` tokens for labels, supporting copy, body text, intros, and card titles. Large headings use responsive sizing.
- Corners: `--radius-sm` (6px) for buttons; `--radius-md` (8px) for callouts; `--radius-lg` (10px) for cards and photographs. Circles are reserved for the engineering diagram.
- Icons: inline SVG with a 24 x 24 viewBox, `.icon`, no fill, currentColor stroke, 1.75 stroke width, and rounded caps/joins. Use `aria-hidden="true"` for icons beside descriptive link text. The initial library is northeast arrow (project links), left arrow (return links), and up arrow (back to top). Reuse their paths from the existing links; use this same geometry and styling for future icons.

Preserve visible keyboard focus. Cards with clipped images keep focus rings inside the linked image. The page canvas stays a single colour; use spacing and borders to separate sections.
## Education and experience timelines

In `index.html`, find `id="experience"`. Education and Experience have separate ordered lists (`ol.timeline`). Keep each list newest first. They appear side by side on desktop and stack on screens 760px wide or smaller.

To add a role, copy the complete `li.timeline-entry` between the EXPERIENCE ENTRY comments and paste it inside the Experience list. For a school, copy the EDUCATION ENTRY block into the Education list. Replace the date range, organization, location, role or degree, overview paragraph, and bullet text. You can add or remove bullets and optional Coursework / Involvement labels.

For an organization logo, put your image in `assets/logos/` (create the folder when needed). Replace the whole `span.timeline-logo` with:

```html
<img class="timeline-logo" src="assets/logos/company.svg" alt="" width="48" height="48">
```

The empty alt avoids repeating the adjacent organization name. Logos fit a 48px square without cropping. The default graduation-cap and briefcase SVGs follow the shared icon library. Retain those when a logo isn't available. Timeline dots and connecting lines are decorative.