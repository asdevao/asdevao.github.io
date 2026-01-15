# Project Overview: Asdevao's Tech Hub

## Purpose
This is a personal technology blog built with Hugo, focusing on:
- Sharing programming experiences and insights
- Exploring AI and technology frontiers
- Documenting coding journey and learning process
- Maintaining a digital knowledge base

## Tech Stack
- **Static Site Generator**: Hugo v0.119+ (configured in hugo.yaml)
- **Theme**: LoveIt theme (customizable Hugo theme)
- **Language**: Chinese (primary) with English support
- **Hosting**: GitHub Pages (configured for https://asdevao.github.io)
- **Features**: 
  - Multilingual support (zh-cn, en)
  - Search functionality (Lunr)
  - Comments (Disqus)
  - Social sharing
  - Reading progress bar
  - Dark/light mode toggle
  - Mermaid diagrams
  - ECharts integration

## Codebase Structure
```
/ (project root)
├── archetypes/          # Content templates
├── assets/             # SCSS, JS, images
├── content/            # Markdown content files
│   ├── posts/         # Blog posts
│   └── _index.md      # Homepage content
├── layouts/            # Custom layout overrides
│   ├── page/          # Page-specific templates
│   └── partials/      # Reusable components
├── public/             # Generated static site (build output)
├── resources/          # Hugo's processed assets
├── static/             # Static assets (images, etc.)
└── themes/LoveIt/     # LoveIt theme (git submodule)
```

## Key Configuration
- `hugo.yaml`: Main site configuration
- `config/_default/`: Additional config files
- Theme parameters in `params:` section of hugo.yaml

## Development Workflow
1. Write content in `content/` as Markdown
2. Customize layouts in `layouts/` if needed
3. Add assets in `assets/` (processed by Hugo Pipes)
4. Build with `hugo` command
5. Serve locally with `hugo server`
6. Deploy by pushing to GitHub (automated via Actions)

## Customizations Made
- Custom archives page layout (simplified to match home page style)
- Footer custom partial
- Multilingual menu configuration