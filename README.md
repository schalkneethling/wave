# Schalk's Profile

A personal VS Code profile extension combining a bespoke colour theme, curated typography defaults, and a hand-picked set of extensions for frontend and web standards development.

## Prerequisites

This extension sets `Monaspace Neon Frozen` as the editor font. You must install the font on your machine before the typography defaults will take effect.

Download it from the [Monaspace GitHub releases page](https://github.com/githubnext/monaspace/releases). Install the fonts prefixed with `MonaspaceNeonFrozen` for your operating system.

Once installed, restart VS Code to ensure the font is picked up correctly.

## What is included

### Neon Wave theme

A dark theme built on a ten-colour palette running from hot pink (`#F72585`) through violet and deep indigo to electric cyan (`#4CC9F0`). The palette is mapped deliberately:

- **Keywords** — hot pink (`#F72585`)
- **Types and classes** — magenta (`#B5179E`)
- **Functions and methods** — sky blue (`#4895EF`)
- **Strings** — cyan (`#4CC9F0`)
- **Variables and properties** — indigo (`#4361EE`)
- **Constants and numbers** — violet (`#7209B7`)
- **Comments** — muted indigo (`#56509A`), italicised
- **Editor background** — deep navy (`#0D0B1E`)

Semantic highlighting is enabled, so token colours adapt to the language server's understanding of the code rather than relying solely on grammar-based TextMate scopes.

### Typography

| Setting | Value |
|---|---|
| Font family | Monaspace Neon Frozen |
| Editor font size | 18px |
| Terminal font size | 16px |
| Line height | 1.7 |
| Ligatures | Enabled (all features via Frozen variant) |

### Extension pack

| Extension | Purpose |
|---|---|
| [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) | Opinionated code formatter |
| [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) | JavaScript and TypeScript linting |
| [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint) | CSS, SCSS, and Less linting |
| [Vite Plus](https://marketplace.visualstudio.com/items?itemName=VoidZero.vite-plus-extension-pack) | Vitest and Oxc tooling for Vite projects |
| [Playwright](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright) | End-to-end and component test runner |
| [CSS Custom Property Inspector](https://marketplace.visualstudio.com/items?itemName=schalkneethling.css-custom-property-inspector) | Inspect and navigate CSS custom properties |
| [CSS VarBuddy](https://marketplace.visualstudio.com/items?itemName=schalkneethling.css-varbuddy) | CSS custom property autocomplete and management |
| [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) | Table of contents, shortcuts, and preview enhancements |
| [VSCode Icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons) | File and folder icon theme |
| [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) | Schema validation, IntelliSense, and formatting |

### Editor defaults

Beyond typography, the following editor preferences are set:

- Format on save enabled for all languages
- Prettier assigned as default formatter for CSS, SCSS, Less, JS, TS, HTML, JSON, and Markdown
- Red Hat YAML assigned as default formatter for YAML files
- Minimap disabled
- Sticky scroll enabled
- Bracket pair colourisation enabled with active pair guides
- Inlay hints set to off unless pressed
- Linked editing enabled (rename paired HTML tags simultaneously)
- Whitespace rendering set to `boundary` (shows spaces at line boundaries only)
- Rulers at 80 and 120 characters
- Smooth scrolling and smooth cursor animation enabled

## Overriding defaults

All settings applied by this extension are defaults. They occupy the lowest priority level in VS Code's settings hierarchy, meaning your user settings and workspace settings will always take precedence. Override anything freely in your `settings.json`.

## Building and installing locally

You will need the `@vscode/vsce` CLI tool:

```sh
npm install -g @vscode/vsce
```

From the root of this repository:

```sh
vsce package
```

This produces a `.vsix` file. Install it with:

```sh
code --install-extension schalkneethling.schalk-profile-1.0.0.vsix
```

Or via the VS Code command palette: **Extensions: Install from VSIX…**

## Licence

MIT