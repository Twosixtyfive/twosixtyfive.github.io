# 🤖 AI Agent System Prompt & Project Manual: twosixtyfive

## 📌 Project Overview
- **Purpose**: A minimalist, tech and privacy-focused blog/guide platform.
- **Tech Stack**: Jekyll (Static Site Generator) hosted on GitHub Pages.
- **Deployment**: Zero-install. GitHub handles the build process upon push to `main`.
- **Design Philosophy**: Modern Minimalist. Focus on high readability, whitespace, and a clean, professional aesthetic.

## 📂 Architecture & Directory Map
| Path | Description | Agent Action/Note |
| :--- | :--- | :--- |
| `_config.yml` | Global site settings | Edit for site-wide variables. |
| `_layouts/` | HTML Structure | Change `default.html` for shell, `post.html` for content. |
| `_posts/` | Content Library | **Strict Naming**: `YYYY-MM-DD-title.md`. |
| `assets/css/` | Visual Layer | Modify `style.css` for theme updates. |
| `index.md` | Home Page | Uses `default` layout; lists recent posts. |
| `about.md` | About Page | Static content page. |
| `blog.md` | Blog Archive | Dynamic list of all `_posts`. |
| `contact.md` | Contact Page | Static content page. |

## 🛠️ Operational Instructions

### ✍️ Creating New Content (Blog/Guides)
To add a new post, the agent **MUST** follow this protocol:
1. **File Path**: `_posts/YYYY-MM-DD-slug.md` (e.g., `_posts/2026-10-28-vpn-guide.md`).
2. **Required Front Matter**:
   ```yaml
   ---
   layout: post
   title: "Human Readable Title"
   date: YYYY-MM-DD
   category: [tech | privacy | general]
   ---
   ```
3. **Content**: Write in standard GitHub Flavored Markdown.

### 🎨 Updating the Visuals
- **Global Theme**: Edit `assets/css/style.css`.
- **Layout Changes**: Edit `_layouts/default.html` for header/footer/navigation.
- **Design Guideline**: Maintain the "Modern Minimalist" look:
  - High contrast for text.
  - Generous padding and whitespace.
  - Soft shadows (`var(--shadow)`) and rounded corners (`var(--radius)`).

### 🚀 Deployment Workflow
1. Stage changes: `git add .`
2. Commit with clear message: `git commit -m "type: description"`
3. Push to main: `git push origin main`

## ⚠️ Critical Constraints
- **No Local Dependencies**: Do not suggest installing Ruby or Jekyll locally unless explicitly asked. Rely on GitHub Pages build.
- **Naming Conventions**: Never deviate from the `YYYY-MM-DD-title.md` format in `_posts/` or the site will fail to build.
- **Layout Consistency**: Ensure all new static pages in the root use `layout: default` in their front matter.
