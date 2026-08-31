# MossyGrave

A CSS design system for Mossy Desk (Tauri + Svelte apps): design tokens,
Nunito self-hosted, and a set of components (buttons, cards, forms,
alerts, modals, sidebar...).

## Philosophy: everything is opt-in

Nothing applies automatically — not even on `<h1>`, `<a>`, `<button>` or
`<input>`. A bare tag renders as plain browser default until you add the
matching class (`.h1`, `.link`, `.button`, `.input`, ...). This keeps the
library safe to drop into any app: nothing you didn't ask for changes,
and no fighting the framework to get a custom element to look custom.

The only page-wide opt-in is `.app` on your root element (theme:
font/colors/background) — everything else is per-element.

```html
<body class="app">
  <h1 class="h1">Title</h1>
  <button class="button button-primary">Go</button>
</body>
```

## Installation

### Manually
Download dist/mossy-grave.min.css and include it in your project:

```html
<link rel="stylesheet" href="path/to/mossy-grave.min.css">
```

## Project Structure
```
mossy-grave/
├── dist/
│   ├── mossy-grave.css       ← Compiled CSS (readable)
│   ├── mossy-grave.min.css   ← Minified CSS (production)
│   └── fonts/                ← Nunito, copied from src/core/fonts/ at build
├── src/
│   ├── core/
│   │   ├── _variables.css    ← Design tokens
│   │   ├── _reset.css        ← Pure structural reset + @font-face (no theme)
│   │   ├── _app-shell.css    ← .app / .selection / .scrollbar / .smooth-scroll
│   │   └── fonts/            ← Nunito woff2 (400/700/900) + OFL.txt
│   ├── components/
│   │   ├── _buttons.css
│   │   ├── _forms.css
│   │   ├── _sidebar.css
│   │   ├── _cards.css
│   │   ├── _typography.css
│   │   ├── _code.css
│   │   ├── _table.css
│   │   ├── _image.css
│   │   ├── _badges.css
│   │   ├── _alerts.css
│   │   └── _modals.css
│   └── mossy-grave.css       ← Main entry point (with @imports, no-build dev mode)
├── examples/
│   └── index.html            ← Usage example
├── package.json
└── README.md
```

## Commands

```bash
# Install dependencies
npm install

# Build the framework (concatenates all CSS files)
npm run build

# Minify the CSS for production
npm run minify

# Build + minify
npm run build:production

# Watch mode (auto-rebuild on changes)
npm run watch
```
