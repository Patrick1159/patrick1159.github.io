# Puyuan Zhang — Academic Homepage

Personal academic homepage and blog, built with [Jekyll](https://jekyllrb.com/) and the [Minimal Light](https://github.com/yaoyao-liu/minimal-light) theme. Hosted on GitHub Pages at [patrick1159.github.io](https://patrick1159.github.io).

## Tech Stack

- **Static site generator:** Jekyll 4.x
- **Theme:** [yaoyao-liu/minimal-light](https://github.com/yaoyao-liu/minimal-light) (via `remote_theme`)
- **Hosting:** GitHub Pages
- **Markdown:** kramdown (GFM)

## Local Development

### Prerequisites

- Ruby 3.x
- Bundler (`gem install bundler`)

### Setup

```bash
# Install dependencies
bundle install

# Start local server
bundle exec jekyll serve

# Start with drafts visible
bundle exec jekyll serve --drafts

# Build for production
bundle exec jekyll build
```

The site will be available at `http://localhost:4000`.

## Blog Workflow

### Writing a Post

1. Create a new file in `_drafts/` (e.g., `my-post.md`)
2. Preview locally with `bundle exec jekyll serve --drafts`
3. When ready, move to `_posts/` and rename to `YYYY-MM-DD-slug.md`
4. Set `published: true` in the front matter
5. Commit and push

### File Naming Convention

```
_posts/YYYY-MM-DD-slug.md
```

Example: `_posts/2026-07-28-robust-perception.md`

### Front Matter Template

```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +0800
excerpt: "A one-sentence summary of the post."
tags:
  - robotics
  - research
lang: en
published: true
---
```

- Use `lang: zh-CN` for Chinese-language posts
- Use `+0800` timezone for dates
- `excerpt` is shown in post listings (explicit is better than auto-truncation)
- `published: false` hides the post from production

### Drafts

Drafts live in `_drafts/`. They are excluded from production builds.

Preview drafts:

```bash
bundle exec jekyll serve --drafts
```

### Publishing

```text
1. Write in _drafts/
2. Preview with --drafts
3. Move to _posts/ with YYYY-MM-DD-slug.md filename
4. Set published: true
5. Commit and push
```

## Deployment

This site is deployed via GitHub Pages. Pushing to the `master` branch triggers an automatic build.

## Personalization Checklist

Before using this site as your public homepage, replace these placeholders:

| Placeholder | Location | Description |
|---|---|---|
| `YOUR_SJTU_EMAIL` | `_config.yml`, `index.md` | Your SJTU academic email |
| `YOUR_GITHUB_USERNAME` | `_config.yml`, `index.md` | Your GitHub username |
| `YOUR_PROGRAM` | `index.md` | Your degree program at SJTU |
| `YOUR_UNDERGRAD_UNIVERSITY` | `index.md` | Your undergraduate institution |
| `YOUR_UNDERGRAD_PROGRAM` | `index.md` | Your undergraduate program |
| `YYYY–YYYY` | `index.md` | Education date ranges |
| `assets/img/avatar.svg` | `_config.yml` | Replace with your actual photo (JPG/PNG) |
| `assets/img/favicon.png` | `_config.yml` | Replace with your favicon |
| CV link | `_config.yml` | Set `cv_link` when CV is available |

## License

Content: All rights reserved.  
Theme: [Minimal Light](https://github.com/yaoyao-liu/minimal-light) is licensed under CC0 1.0 Universal.
