# Code Style and Conventions

- **Hugo Templates**: Use Go template syntax in `.html` files within `layouts/`
- **Naming**: 
  - Layouts: `_default/`, `partials/`, `page/`
  - Partials: snake_case with `.html` extension
- **HTML**: Standard HTML5, with Hugo helpers like `{{ . }}`, `{{- partial -}}`
- **CSS**: Follow theme conventions, custom styles in partials
- **JavaScript**: 
  - Vanilla JS, no frameworks
  - Use `document.addEventListener('DOMContentLoaded', ...)`
  - Event listeners for interactivity
  - DOM manipulation for dynamic content
- **Markdown**: Standard Markdown with Hugo frontmatter (YAML)
- **Comments**: HTML `<!-- -->`, JS `//` or `/* */`
- **Indentation**: 2 spaces for HTML/JS, 4 spaces for YAML
- **File Organization**: 
  - Custom layouts in `layouts/` override theme
  - Static assets in `static/`
  - Content in `content/` with `_index.md` for sections