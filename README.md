# Software Walker (GitHub Pages)

This is the static version of the **Software Walker** blog, built using Jekyll and ready to host on GitHub Pages.

## Project Structure

*   `_posts/` — Contains all 40 blog posts converted to clean Markdown.
*   `assets/images/` — Self-hosted copies of all media assets downloaded from the original WordPress site.
*   `about/` and `about/projects/` — Custom page structures for "About Bill" and "Projects".
*   `_layouts/` — HTML layout templates (`default.html`, `post.html`, `page.html`).
*   `assets/css/style.css` — Custom, clean, mobile-responsive styling sheet (supports prefers-color-scheme dark/light).
*   `_config.yml` — Global site parameters and settings.

---

## Local Development

To run the site locally and preview your changes:

1.  **Install Ruby dependencies:**
    Make sure you have Ruby installed on your Mac, then run:
    ```bash
    bundle install
    ```

2.  **Start the local Jekyll server:**
    ```bash
    bundle exec jekyll serve
    ```

3.  **Preview the site:**
    Open your browser and navigate to `http://localhost:4000/`.

---

## How to Add a New Post

To create a new blog post, simply write a new Markdown file and save it in the `_posts/` directory.

### Filename Pattern
`YYYY-MM-DD-your-post-title.md` (e.g., `2026-07-02-hello-github-pages.md`).

### Post Frontmatter template
At the very top of your markdown file, include the following metadata:
```markdown
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS -0700
categories: ["software", "development"]
tags: ["git", "jekyll"]
---

Your post content in standard Markdown goes here...
```

---

## Publishing Changes

Once you've committed your new posts or changes, simply push them to your GitHub repository:

```bash
git add .
git commit -m "Add new post: Hello GitHub Pages"
git push origin main
```

GitHub Pages will automatically build the site and publish it to `https://softwarewalker.com/`.
