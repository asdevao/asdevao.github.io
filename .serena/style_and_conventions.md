# Code Style and Conventions for Hugo Blog

## Hugo Template Conventions
- Use Go template syntax: `{{ .Variable }}`, `{{- range .Items -}}`
- Use `{{- -}}` for whitespace control to avoid unwanted spaces
- Follow Hugo's context scoping with `.` for current context

## Naming Conventions
- Variables: camelCase (e.g., `homeProfile`, `pageTitle`)
- CSS Classes: kebab-case (e.g., `home-profile`, `page-title`)
- Template Functions: camelCase (e.g., `partial`, `render`)

## Internationalization
- Use `i18n "key"` for translatable strings
- Provide defaults with `| default "fallback text"`
- Support both English and Chinese as configured

## Layout Structure
- Main layout in `layouts/_default/baseof.html`
- Page-specific layouts in `layouts/page/`
- Partials in `layouts/partials/`
- Override theme layouts by matching file paths

## Content Organization
- Posts in `content/posts/`
- Pages in `content/` root or subdirectories
- Front matter uses YAML (configured in hugo.yaml)

## CSS and JS
- Custom styles in `assets/css/`
- Custom scripts in `assets/js/`
- Use Hugo Pipes for processing: `{{ $css := resources.Get "css/main.css" | resources.Minify }}`

## Best Practices
- Use Hugo's built-in functions over custom logic when possible
- Leverage theme's CSS classes for consistency
- Keep templates DRY by using partials
- Test layouts across different content types