# roboav8r.github.io

Personal site and Arwun build log. Built with plain Jekyll (no theme gem) so GitHub
Pages compiles it automatically — there's nothing to build yourself.

## Deploy (one time)

1. Create a **public** repo named exactly `roboav8r.github.io`.
2. Drop these files at the repo root and push to `main`.
3. Repo **Settings → Pages → Build and deployment**: set Source to
   **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. Wait ~1 minute. The site is live at https://roboav8r.github.io.

No `.nojekyll` file — we *want* Jekyll to run.

## Add a build-log entry

Create a file in `_posts/` named `YYYY-MM-DD-some-title.md`:

```markdown
---
layout: post
title: "Your title"
date: 2026-06-20
summary: "One line shown in the log list."
tags: [arwun, isaac]
---

Write the entry in Markdown here.
```

It appears automatically on `/log/` and the homepage, newest first.

## Edit the rest

- `index.html` — landing page / hero
- `projects.md` — project entries (search for `TODO`)
- `resume.md` — resume (stub; fill from your real resume)
- `assets/css/main.css` — all styling lives in the `:root` tokens at the top
- `_config.yml` — title, tagline, social handles

## Preview locally (optional)

### Prerequisites

- Ruby 3.x (with a C toolchain to build native gems — on Debian/Ubuntu:
  `sudo apt install ruby-full build-essential zlib1g-dev`)
- Bundler: `gem install bundler`

Gem dependencies (Jekyll, GitHub Pages, etc.) are pinned in the `Gemfile` —
no separate requirements file needed.

### Run

```bash
bundle install
bundle exec jekyll serve --livereload
# http://localhost:4000
```
