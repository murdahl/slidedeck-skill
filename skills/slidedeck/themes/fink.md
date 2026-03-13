# Fink Theme

When the user asks for a "fink" theme, apply these overrides plus the additional font import and gradient tweaks.

## Font Import

Add this `@import` at the top of the `<style>` block (exception to the no-CDN rule — fonts only):

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500&display=swap');
```

## CSS Variable Overrides

```css
:root {
  --font-heading: 'HK Grotesk', 'DM Sans', system-ui, -apple-system, sans-serif;
  --font-body: 'Roboto', system-ui, -apple-system, sans-serif;
  --color-bg: #F0E6C8;
  --color-surface: #DCE8D0;
  --color-primary: #1E3A34;
  --color-primary-light: #2D5A50;
  --color-accent: #EDBFA6;
  --color-text: #000000;
  --color-text-muted: #3D3D3D;
  --color-border: #C8D4BE;
}
```

## Palette Reference

Use for slide backgrounds, cards, accents:

- Pale Sun (warm cream): `#F0E6C8` — default background
- Pale Lime (soft green): `#DCE8D0` — surface / cards
- Blush (peach): `#EDBFA6` — accent / highlights
- Earth (warm pink): `#F0C4AA` — alternate accent
- Moss (dark teal): `#1E3A34` — primary / headings / strong contrast
- Light Blue: `#C4DDE8` — info / alternate background

## Style Overrides

Add after the theme variables:

```css
/* Fink: headings use medium weight with letter-spacing */
.slide-title h1 {
  font-weight: 500;
  letter-spacing: 0.02em;
  background: none;
  -webkit-background-clip: unset;
  -webkit-text-fill-color: var(--color-primary);
}
.slide-title {
  background: var(--color-bg);
}
.slide-content h2, .slide-split h2, .slide-code h2 {
  color: var(--color-primary);
  letter-spacing: 0.02em;
}
/* Fink: progress bar uses moss solid */
.progress-bar {
  background: var(--color-primary);
}
/* Fink: overview border uses moss */
.deck.overview .slide-thumb.active { border-color: var(--color-primary); box-shadow: 0 0 0 2px rgba(30,58,52,0.3); }
.deck.overview .slide-thumb:hover { border-color: var(--color-primary); }
```

## Logo SVG

Embed inline when the user wants branding:

```html
<!-- Small fink bird logo — use in title slide .meta or as a standalone element -->
<svg class="fink-logo" width="40" height="39" viewBox="0 0 57 55" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M2.578 6.963a.326.326 0 0 0 .237-.349C2.999 5.17 4.19.575 11.61.575c5.511 0 7.654 4.139 8.468 6.855.512 1.71 1.4 3.273 2.619 4.54l32.747 34.059c.313.326.024.874-.41.774l-17.168-3.904a.326.326 0 0 0-.208.014c-2.082.567-31.708 8.929-35.168-14.1C1.142 19.849 2.913 12.248 2.926 11.42c.003-.13-.3-.643-.39-.732L.715 8.647a.326.326 0 0 1 .1-.745l1.762-.94Z" stroke="#1E3A34" stroke-width="1.15" stroke-miterlimit="10"/>
  <path d="m26.365 44.755-4.642 8.82h-4.995" stroke="#1E3A34" stroke-width="1.15" stroke-miterlimit="10" stroke-linecap="round"/>
  <path d="m20.6 44.755-4.642 8.82h-4.995" stroke="#1E3A34" stroke-width="1.15" stroke-miterlimit="10" stroke-linecap="round"/>
  <path d="M2.655 13.291a29.8 29.8 0 0 0 .764-.088 6.326 6.326 0 0 0 3.216-2.604c.124-.331.293-.5.591-.311.92.583 2.896.346 3.533-.978C11.874 6.99 20.335 22.205 27.49 16.95" stroke="#1E3A34" stroke-width="1.15" stroke-miterlimit="10"/>
  <path d="M44.446 34.59S22.324 47.276 10.121 29.484" stroke="#1E3A34" stroke-width="1.15" stroke-miterlimit="10" stroke-linecap="round"/>
</svg>
```
