---
name: make-blog-post
description: Create a new Jekyll blog post for this site from a title and body, then proofread it, branch, commit, push, and open a draft PR. Use when the user wants to publish or draft a new blog/log entry (e.g. "/make-blog-post", "write a blog post", "add a log entry").
---

# Make a blog post

Turn a title and body into a new Jekyll post for this site, review it editorially, then
put it on a branch and open a draft PR for the user to review.

This is the `roboav8r.github.io` Jekyll site. Posts live in `_posts/` and are published as
`YYYY-MM-DD-<slug>.md`. They render automatically in the `/log/` build-log index at
`/log/<slug>/` (the date is not part of the URL — the slug is).

## Inputs
- **Title** (required) and **body** (required). Both usually come in with the invocation.
  If either is missing, ask for it before doing anything else.
- **summary** and **tags** are optional. If the user supplies them explicitly, use them
  verbatim. Otherwise derive them (see step 3).

## Workflow

### 1. Gather inputs
Confirm you have a title and a body. Don't proceed without both.

### 2. Editorial review — do this BEFORE creating any files
Act as the user's editor on the submitted body:
- Fix spelling, grammar, and punctuation.
- Flag anything unclear, awkward, or wordy and suggest tighter phrasing.
- Match the site's voice: read `_posts/2026-07-18-hello-world.md` for reference — it's a
  casual, concise "build log" tone. Keep the author's voice; don't corporate-ify it.
- Call out any factual or technical claims that look questionable or unverifiable — ask,
  don't guess.
- Present a corrected draft plus a short bulleted list of the notable suggestions, then let
  the user accept, tweak, or override. **Suggest; don't silently rewrite substance or
  invent facts.** Only continue once the user is happy with the text.

### 3. Compute values
- **date**: today in the site timezone. Run `TZ=America/New_York date +%F` — don't assume.
- **slug**: from the title — lowercase, replace every run of non-alphanumeric characters
  with a single hyphen, and trim leading/trailing hyphens. (e.g. "Hello, World!" → `hello-world`).
- **summary** (if not user-supplied): one concise sentence capturing the post, in the
  site's voice.
- **tags** (if not user-supplied): 1–3 short lowercase tags, inline-array form like `[meta]`.

### 4. Create the post file
Write `_posts/<date>-<slug>.md` with frontmatter matching the existing convention exactly
(note it's `summary`, not `excerpt`/`description`):

```
---
layout: post
title: "<title>"
date: <date>
summary: "<summary>"
tags: [<tags>]
---

<edited body>
```

### 5. Branch, commit, push
Work off an up-to-date `main`:
- If the working tree is dirty, warn the user before switching branches — don't blow away
  their changes.
- `git checkout main` and `git pull` (best effort — if the pull fails offline, continue).
- `git checkout -b blog/<date>-<slug>`.
- Stage **only the new post file** — `git add _posts/<date>-<slug>.md`. Never `git add .`.
- Commit with message `Add blog post: <title>` and the standard trailer:

  ```
  Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>
  ```
- `git push -u origin blog/<date>-<slug>`.

### 6. Open a draft PR
Use `gh pr create --draft --base main` with:
- title = the post title,
- a body that summarizes the post and notes it will render at `/log/<slug>/`, ending with:

  ```
  🤖 Generated with [Claude Code](https://claude.com/claude-code)
  ```

If `gh` is unavailable or not authenticated, fall back to just pushing the branch and
printing the compare URL for the user to open the PR manually.

### 7. Report
Tell the user the branch name and the PR (or compare) URL.

## Guardrails
- Only ever commit the single new post file.
- Branch name and filename share the same `<date>-<slug>` for consistency.
- Don't fabricate facts or alter the meaning of the user's content during the edit pass.
