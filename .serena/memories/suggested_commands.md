# Suggested Commands for Development

## Building and Serving
- `hugo`: Build the site to `public/` directory
- `hugo server`: Start local development server (usually on localhost:1313)
- `hugo server -D`: Include draft content in development

## Version Control
- `git status`: Check current status
- `git add .`: Stage all changes
- `git commit -m "message"`: Commit changes
- `git push`: Push to remote (GitHub Pages)

## Windows Specific
- Use PowerShell or Command Prompt
- `dir` instead of `ls` (though `ls` may work in some terminals)
- Paths use backslashes `\` but forward slashes `/` work in most commands

## Deployment
- After `hugo`, commit and push `public/` for GitHub Pages
- Or use GitHub Actions for automated deployment

## Other
- No linting/formatting tools configured
- Manually check HTML/JS syntax
- Use browser dev tools for debugging