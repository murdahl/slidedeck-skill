# Style Presets

Additional style presets beyond the 5 built-in themes. Each preset includes a mood description, font pairing, color palette, and animation feel. Apply by overriding CSS variables in `:root`.

## Mood Mapping

| Preset | Mood | Best For |
|--------|------|----------|
| Bold Signal | Confident, high-energy | Keynotes, launches, pitches |
| Neon Cyber | Futuristic, techy | Dev talks, hackathons, tech demos |
| Paper & Ink | Thoughtful, literary | Storytelling, case studies, essays |
| Swiss Modern | Minimal, precise | Data presentations, reports, analysis |

---

## Bold Signal

High contrast, keynote-ready. Big type, strong colors, punchy transitions.

**Font Pairing:** `Inter` (headings 900 weight) + `Inter` (body 400)

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');

:root {
  --font-heading: 'Inter', system-ui, sans-serif;
  --font-body: 'Inter', system-ui, sans-serif;
  --color-bg: #000000;
  --color-surface: #111111;
  --color-primary: #ff3366;
  --color-primary-light: #ff6b8a;
  --color-accent: #ffcc00;
  --color-text: #ffffff;
  --color-text-muted: #aaaaaa;
  --color-border: #333333;
  --transition: 0.3s cubic-bezier(0.16, 1, 0.3, 1);
}

.slide-title h1 {
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: -0.02em;
  background: linear-gradient(135deg, #ff3366, #ffcc00);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

---

## Neon Cyber

Dark base with vibrant neon accents. Glow effects and sharp edges.

**Font Pairing:** `Space Grotesk` (headings) + `JetBrains Mono` (body)

```css
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;700&family=JetBrains+Mono:wght@400;500&display=swap');

:root {
  --font-heading: 'Space Grotesk', system-ui, sans-serif;
  --font-body: 'JetBrains Mono', monospace;
  --font-mono: 'JetBrains Mono', monospace;
  --color-bg: #0a0a1a;
  --color-surface: #12122a;
  --color-primary: #00ffaa;
  --color-primary-light: #33ffbb;
  --color-accent: #ff00ff;
  --color-text: #e0e0ff;
  --color-text-muted: #7777aa;
  --color-border: #222244;
  --radius: 4px;
  --transition: 0.35s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.slide-title h1 {
  text-shadow: 0 0 40px rgba(0, 255, 170, 0.3), 0 0 80px rgba(0, 255, 170, 0.1);
  background: linear-gradient(135deg, #00ffaa, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.slide-code pre {
  border: 1px solid #00ffaa33;
  box-shadow: 0 0 20px rgba(0, 255, 170, 0.05);
}
```

---

## Paper & Ink

Warm, literary feel. Serif typography with generous whitespace.

**Font Pairing:** `Playfair Display` (headings) + `Source Serif 4` (body)

```css
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Source+Serif+4:wght@400;600&display=swap');

:root {
  --font-heading: 'Playfair Display', Georgia, serif;
  --font-body: 'Source Serif 4', Georgia, serif;
  --font-mono: 'SF Mono', 'Fira Code', monospace;
  --color-bg: #faf7f2;
  --color-surface: #f0ece4;
  --color-primary: #8b4513;
  --color-primary-light: #a0522d;
  --color-accent: #c17817;
  --color-text: #2c2416;
  --color-text-muted: #6b5e4f;
  --color-border: #d4cec4;
  --radius: 2px;
  --transition: 0.5s ease;
}

.slide-title h1 {
  font-weight: 900;
  font-style: italic;
  background: none;
  -webkit-text-fill-color: var(--color-text);
}

.slide-title {
  background: none;
}

.progress-bar {
  background: var(--color-primary);
}
```

---

## Swiss Modern

Clean, grid-aligned, data-forward. Inspired by Swiss/International style.

**Font Pairing:** `DM Sans` (headings) + `DM Sans` (body)

```css
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');

:root {
  --font-heading: 'DM Sans', Helvetica, Arial, sans-serif;
  --font-body: 'DM Sans', Helvetica, Arial, sans-serif;
  --color-bg: #ffffff;
  --color-surface: #f5f5f5;
  --color-primary: #0055ff;
  --color-primary-light: #3377ff;
  --color-accent: #ff0044;
  --color-text: #111111;
  --color-text-muted: #666666;
  --color-border: #e0e0e0;
  --radius: 0px;
  --transition: 0.25s ease;
}

.slide-title h1 {
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  background: none;
  -webkit-text-fill-color: var(--color-text);
}

.slide-title {
  background: none;
  align-items: flex-start;
  text-align: left;
  padding-left: 10%;
}

.progress-bar {
  background: var(--color-primary);
  height: 3px;
}
```
