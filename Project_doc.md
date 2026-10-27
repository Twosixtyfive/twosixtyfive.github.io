# Project Documentation: twosixtyfive Site

## Architecture
This site is built using **Jekyll**, a static site generator that is natively supported by GitHub Pages. This allows for "zero-install" deployment—content is pushed as Markdown, and GitHub builds the HTML automatically.

## Directory Structure
- `_config.yml`: Global site settings.
- `_layouts/`: HTML templates.
  - `default.html`: The main shell (header, footer, CSS links).
  - `post.html`: The layout for individual blog posts/guides.
- `_posts/`: Markdown files for blog entries. Files must follow the naming convention: `YYYY-MM-DD-title.md`.
- `assets/css/`: Global styles.
- `index.md`, `about.md`, etc.: Static pages using the `default` layout.

## Content Management
### Adding a New Post/Guide
1. Create a new file in `_posts/` named `YYYY-MM-DD-your-title.md`.
2. Add "Front Matter" at the top of the file:
   ```markdown
   ---
   layout: post
   title: "Your Title Here"
   date: 2026-10-27
   category: tech
   ---
   ```
3. Write your content in Markdown below the front matter.

### Updating the Theme
- Edit `assets/css/style.css` for global visual changes.
- Edit `_layouts/default.html` to change the site's overall structure.

## Deployment
No local build process is required. Simply push changes to the `main` branch on GitHub, and GitHub Pages will automatically trigger a Jekyll build.
