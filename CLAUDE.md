# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git workflow

Always commit and show the summary first, then **ask before pushing**. Only push after explicit confirmation. The only exception is if the user says "commit and push" in the same message.

## What this is

Elinor's personal academic website (`elinorp-d.github.io`), built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme. Deployed automatically to GitHub Pages from the `main` branch — `gh-pages` is auto-generated, never edit it directly. No local preview setup; changes go live after pushing to `main` (~4 min build).

## Common update tasks

Use the project slash commands for the most frequent tasks:
- `/add-paper` — add a publication to papers.bib + create a news item
- `/add-news` — add a standalone news announcement
- `/update-cv` — update the CV PDF on the site

## Content locations

| What | Where |
|------|--------|
| Bio / about page | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` |
| News items | `_news/announcement_N.md` (numbered sequentially; currently up to 13) |
| Projects | `_projects/*.md` |
| Blog posts | `_posts/YYYY-MM-DD-title.md` |
| CV PDF | `assets/pdf/Elinor_Poole_Dayan_CV_[Mon][YY].pdf` — download from Overleaf to ~/Downloads, then run `/update-cv` (also copies to Dropbox Resumes folder) |
| CV page | `_pages/cv.md` — `cv_pdf:` field and `description:` ("Last updated ...") |
| CV source | Overleaf project at `~/Dropbox/Apps/Overleaf/Elinor_Poole-Dayan_CV_*/` (only .tex syncs, not compiled PDF) |
| Co-author links | `_data/coauthors.yml` |
| Venue badges | `_data/venues.yml` |
| Site-wide config | `_config.yml` |

## Publications (papers.bib)

The file has a YAML front matter block (`---`) at the top — don't remove it.

**Entry types used:** `@inproceedings` (conferences), `@misc` (arXiv preprints, workshop papers), `@mastersthesis`

**Fields to always include:**
- `arxiv`, `eprint`, `archivePrefix`, `primaryClass`, `url` — for any paper on arXiv
- `abbr` — must **exactly match** a key in `_data/venues.yml` to get a badge+link; add new venues to that file first
- `abstract` — always include
- `selected` — `true` only for flagship papers shown on the homepage

**Optional fields that generate buttons:** `code`, `dataset`, `demo`, `pdf`, `poster`, `slides`, `website`, `html`

**Other special fields:** `press` (media coverage — renders as a visible block below the buttons; Markdown OK, e.g. `Covered by [MIT News](url), [CACM](url).`), `additional_info` (venue footnotes, workshop notes — renders inline on the periodical/venue line), `annotation` (popover after author list)

**New venue in venues.yml format:**
```yaml
"VENUE ABBR YEAR":
  color: "#hexcode"
  url: https://venue-url.org/
```

**New co-author in coauthors.yml format** (key = lowercase last name, no accents):
```yaml
"lastname":
  - firstname: ["First", "F.", "First Last", "F Last"]
    url: https://their-website.com/
```

## News items

Format (`_news/announcement_N.md`):
```markdown
---
layout: post
date: YYYY-MM-DD
inline: true
related_posts: false
---

News text here with [links](url) in Markdown.
```

Always add a news item when adding a paper (paper accepted, preprint posted, etc.). Use the next sequential number.

## Styling

- Theme color: `_sass/_themes.scss` (`--global-theme-color`)
- Variables (fonts, spacing): `_sass/_variables.scss` and `_sass/_base.scss`
