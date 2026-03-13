# Slidedeck Skill for Claude Code

A custom Claude Code skill that generates single-file HTML slide decks with all CSS and JS inline. No external dependencies.

## Features

- Self-contained `.html` files — just open in a browser
- Full keyboard navigation (arrows, Home/End, number keys)
- Touch/swipe support
- Overview mode (press `O`)
- Fullscreen mode (press `F`)
- Print/PDF export support
- 5 built-in themes: **dark**, **light**, **warm**, **green**, **fink**
- Slide types: Title, Content, Split, Code, Embed, Image

## Installation

### Claude Code (CLI)

**Personal (all projects):**

```bash
# Copy the skill to your personal skills directory
mkdir -p ~/.claude/skills/slidedeck
cp -r skills/slidedeck/* ~/.claude/skills/slidedeck/
```

**Project-level (this project only):**

```bash
# Copy the skill to the project's .claude directory
mkdir -p .claude/skills/slidedeck
cp -r skills/slidedeck/* .claude/skills/slidedeck/
```

After installation, Claude will automatically invoke the skill when you ask to create a slide deck or presentation.

### Claude Desktop

Claude Desktop discovers skills from the same locations as the CLI. To install:

1. Copy the skill directory to `~/.claude/skills/slidedeck/`
2. Open Claude Desktop
3. The skill is automatically available — just ask Claude to create a slide deck

Skills are shared between Claude Code CLI, Claude Desktop, and the VS Code extension.

## Usage

Just ask Claude naturally:

> "Create a 10-slide presentation about our Q4 results with fink theme"

> "Make a technical talk about React Server Components in Norwegian"

Claude auto-invokes the skill when it detects you want a slide deck or presentation.

### Themes

Request a theme by name in your prompt:

| Theme | Description |
|-------|-------------|
| `dark` | Default dark blue/purple theme |
| `light` | Clean white background |
| `warm` | Dark with orange/red accents |
| `green` | Dark green with emerald accents |
| `fink` | Warm cream with moss teal — includes Fink bird logo |

## File Structure

```
skills/slidedeck/
├── SKILL.md              # Skill instructions and slide engine boilerplate
└── themes/
    ├── dark.md           # Default dark theme
    ├── light.md          # Light theme overrides
    ├── warm.md           # Warm theme overrides
    ├── green.md          # Green theme overrides
    └── fink.md           # Full Fink theme with logo SVG
```

## Output

The skill writes a single `.html` file to the current working directory with a descriptive kebab-case filename (e.g., `ai-workshop-fink.html`). Open it directly in any browser.

## Navigation

| Key | Action |
|-----|--------|
| `→` / `Space` | Next slide |
| `←` | Previous slide |
| `Home` / `↑` | First slide |
| `End` / `↓` | Last slide |
| `O` | Toggle overview |
| `F` | Toggle fullscreen |
| `1`-`9` | Jump to slide |
