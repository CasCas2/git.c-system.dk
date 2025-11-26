# CLAUDE.MD

This file provides context for Claude Code when working on this project.

## Project Overview

This is a Hugo static site generator project for **C-System.dk**, using the **hello-friend-ng** theme. The site is configured to support multiple languages (English, Danish, French) and is published to https://git.c-system.dk.

## Technology Stack

- **Static Site Generator**: Hugo
- **Theme**: hello-friend-ng
- **Languages**: English (en), Danish (da), French (fr)
- **Hosting URL**: https://git.c-system.dk

## Project Structure

```
.
├── archetypes/          # Content templates for new posts
├── content/             # Site content (posts, pages)
│   ├── about.md        # About page
│   └── posts/          # Blog posts in multiple languages
├── layouts/            # Custom layout overrides
├── static/             # Static assets (images, css, js, favicons)
├── themes/             # Theme files
│   └── hello-friend-ng/
├── public/             # Generated static site (don't edit manually)
├── resources/          # Hugo-generated resources cache
└── config.toml         # Site configuration
```

## Key Configuration

- **Base URL**: https://git.c-system.dk
- **Theme**: hello-friend-ng
- **Pagination**: 10 items per page
- **Syntax Highlighting**: Monokai theme with code fences enabled
- **License**: Creative Commons Attribution-NonCommercial 4.0 International

## Common Tasks

### Development

```bash
# Start local development server with drafts
hugo server -D

# Start server without drafts
hugo server

# Build the site
hugo
```

### Content Creation

```bash
# Create a new post
hugo new posts/my-new-post.md

# Create a post in a specific language
hugo new posts/my-new-post.fr.md  # French
hugo new posts/my-new-post.da.md  # Danish
```

### Building and Deployment

```bash
# Build for production (outputs to public/)
hugo --minify

# Clean build
rm -rf public/ && hugo --minify
```

## Content Guidelines

- Posts are located in `content/posts/`
- Use front matter for metadata (title, date, draft status, tags, categories)
- Multi-language posts use language codes as file extensions: `.en.md`, `.fr.md`, `.da.md`
- Images and static assets go in the `static/` directory
- Custom layouts override theme defaults and go in `layouts/`

## Configuration Notes

- Permalinks follow pattern: `/posts/:year/:month/:title/`
- Theme toggle is currently disabled (`enableThemeToggle = false`)
- Sharing buttons are enabled
- Global language menu is enabled
- RSS feed is enabled with limit of 10 items

## Important Files

- `config.toml` - Main site configuration
- `content/about.md` - About page content
- `layouts/` - Custom layout overrides (if any)
- `static/` - Favicon and other static assets

## Customization

The site can be customized through:
- `config.toml` for site-wide settings
- Custom CSS/JS via `params.customCSS` and `params.customJS`
- Layout overrides in `layouts/` directory
- Favicon colors in `params.favicon.color` section

## Branch Information

- **Current branch**: cool-villani
- **Main branch**: main
- **Repository**: Git worktree setup

## Notes for Claude

When making changes:
- Always test locally with `hugo server` before building
- Check that changes work across all configured languages
- Maintain consistent formatting in TOML configuration
- Don't edit files in `public/` directory (auto-generated)
- Theme files in `themes/hello-friend-ng/` should not be modified directly - use layout overrides instead
