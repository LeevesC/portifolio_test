# vCard Portfolio - SCSS Version

A modern, responsive personal portfolio website built with HTML, CSS (compiled from SCSS), and vanilla JavaScript.

## SCSS Structure

The CSS has been converted to SCSS and organized into modular files for better maintainability:

```
assets/scss/
├── style.scss               # Main SCSS file (imports all modules)
├── _variables.scss          # SCSS variables (colors, typography, shadows, etc.)
├── _base.scss               # Base styles (reset, typography, keyframes)
├── _layout.scss             # Layout components (main structure, sidebar)
├── _components.scss         # Reusable components (buttons, cards, forms, etc.)
├── _pages.scss              # Page-specific styles (about, resume, portfolio, blog, contact)
└── responsive/              # Responsive styles organized by breakpoint
    ├── _index.scss          # Main responsive file (imports all breakpoints)
    ├── _small.scss          # Small screens (450px+)
    ├── _medium.scss         # Medium screens (580px+)
    ├── _tablet.scss         # Tablet screens (768px+)
    ├── _desktop.scss        # Desktop screens (1024px+)
    └── _large.scss          # Large screens (1250px+)
```

## Features

- **Modular SCSS Architecture**: Well-organized SCSS files for easy maintenance
- **Organized Responsive Folder**: All responsive styles in a dedicated folder
- **Breakpoint-Specific Files**: Each responsive breakpoint has its own dedicated file
- **Modern SCSS Syntax**: Uses `@use` instead of deprecated `@import`
- **Responsive Design**: Mobile-first approach with organized breakpoint files
- **SCSS Variables**: Centralized color scheme, typography, and spacing
- **Component-based**: Reusable SCSS components and mixins

## Responsive Breakpoints

The responsive design is organized into separate files for each breakpoint under the `responsive/` folder:

| File                       | Breakpoint | Description                       |
| -------------------------- | ---------- | --------------------------------- |
| `responsive/_small.scss`   | 450px+     | Small mobile improvements         |
| `responsive/_medium.scss`  | 580px+     | Medium screens and larger mobiles |
| `responsive/_tablet.scss`  | 768px+     | Tablet and small desktop          |
| `responsive/_desktop.scss` | 1024px+    | Desktop and larger screens        |
| `responsive/_large.scss`   | 1250px+    | Large desktop screens             |

## Development

### Prerequisites

- Node.js and npm installed
- SASS compiler (included as dev dependency)

### Setup

1. Install dependencies:

```bash
npm install
```

2. Compile SCSS to CSS:

```bash
npm run sass
```

3. Watch for SCSS changes (auto-compile):

```bash
npm run sass:watch
```

4. Start development server:

```bash
python3 -m http.server 3000
```

### SCSS Compilation

The project includes npm scripts for SCSS compilation:

- `npm run sass` - Compile SCSS once
- `npm run sass:watch` - Watch for changes and auto-compile

### File Structure

- `assets/scss/` - SCSS source files
- `assets/css/style.css` - Compiled CSS output
- `index.html` - Main HTML file
- `assets/js/script.js` - JavaScript functionality
- `assets/images/` - Image assets

## SCSS Variables

Key SCSS variables are defined in `_variables.scss`:

- **Colors**: Brand colors, gradients, and semantic color tokens
- **Typography**: Font families, sizes, and weights
- **Spacing**: Consistent spacing scale
- **Shadows**: Box shadow definitions
- **Breakpoints**: Responsive design breakpoints
- **Transitions**: Animation timing functions

## Working with Responsive Design

### Modular Approach

Each breakpoint has its own file, making it easy to:

- Focus on specific screen sizes
- Maintain and debug responsive styles
- Collaborate on different breakpoints
- Keep files manageable in size

### Adding New Responsive Styles

To add responsive styles:

1. **For existing breakpoints**: Edit the appropriate file in the `responsive/` folder (e.g., `responsive/_medium.scss`)
2. **For new breakpoints**:
   - Create a new file in the `responsive/` folder (e.g., `responsive/_custom.scss`)
   - Add `@use 'custom';` to `responsive/_index.scss`

### Mixin Usage (Optional)

You can still use the responsive mixin for ad-hoc responsive styles:

```scss
.my-component {
  @include respond-to(medium) {
    // Custom styles for medium+ screens
  }
}
```

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers
- CSS Grid and Flexbox support required

## License

This project is open source and available under the [MIT License](LICENSE).
