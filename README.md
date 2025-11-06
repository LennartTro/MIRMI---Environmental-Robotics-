# MIRMI — Environmental Robotics Lab

This repository hosts the lab website built with Jekyll for GitHub Pages.

## Structure
- `_config.yml` — Site configuration (title, baseurl, build settings)
- `_layouts/` — Page and post layouts
- `_includes/` — Reusable HTML snippets (navigation)
- `_data/` — YAML data for people, projects, publications
- `_posts/` — News posts (blog format)
- `index.md`, `people.md`, `projects.md`, `publications.md`, `news.md`, `contact.md`
- `assets/` — Styles and JavaScript

## Editing Content
- People: edit `_data/people.yml`
- Projects: edit `_data/projects.yml`
- Publications: edit `_data/publications.yml`
- News: add new posts to `_posts/YYYY-MM-DD-title.md`

## GitHub Pages
1. Push to GitHub and enable Pages: Settings → Pages → "Deploy from a branch" → select `main` and `/ (root)`.
2. Optional custom domain: add your domain in Settings → Pages and create DNS records.
3. Update `_config.yml` with your `url` and `baseurl` if needed.

### Custom Domain (optional)
- Subdomain `lab.example.com`: create a CNAME to `USERNAME.github.io` and add a `CNAME` file with `lab.example.com`.
- Apex `example.com`: create A records to GitHub Pages IPs (see GitHub Docs). Enable HTTPS.

## Local Preview (optional)
To build locally you can install Jekyll and run `bundle exec jekyll serve`. This is optional; GitHub Pages builds automatically.
