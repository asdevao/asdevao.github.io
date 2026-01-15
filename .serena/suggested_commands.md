# Suggested Commands for Hugo Blog Development

## Building the Site
- `hugo`: Build the static site to the `public/` directory
- `hugo --minify`: Build with minified output

## Local Development Server
- `hugo server`: Start development server with live reload at http://localhost:1313
- `hugo server --buildDrafts`: Include draft posts in the build

## Creating New Content
- `hugo new posts/new-post.md`: Create a new blog post
- `hugo new page/new-page.md`: Create a new page

## Git Workflow
- `git add .`: Stage all changes
- `git commit -m "message"`: Commit changes
- `git push`: Push to remote repository

## Deployment (GitHub Pages)
- Build the site with `hugo` then push the `public/` directory contents

## Theme Updates
- Update LoveIt theme via git submodule: `git submodule update --remote themes/LoveIt`

## Configuration
- Edit `hugo.yaml` for site configuration
- Custom layouts in `layouts/` override theme defaults