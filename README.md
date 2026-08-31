# MossyGrave
A CSS Boilerplate for my future project: Mossy Desk.
## Installation

### With npm

```bash
npm install mossy-grave
```

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
│   └── mossy-grave.min.css   ← Minified CSS (production)
├── src/
│   ├── core/
│   │   ├── _variables.css    ← CSS variables
│   │   └── _reset.css        ← Base styles
│   ├── components/
│   │   ├── _buttons.css
│   │   ├── _forms.css
│   │   ├── _sidebar.css
│   │   ├── _cards.css
│   │   ├── _typography.css
│   │   ├── _badges.css
│   │   ├── _alerts.css
│   │   └── _modals.css
│   └── mossy-grave.css       ← Main entry point (with @imports)
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