# personal-journal

Source content for **[lxuu.dev](https://www.lxuu.dev/)**—the project listings and write-ups you see on that site are built from this repository.

Each **project** is an `.mdx` file under `projects/` with YAML **frontmatter** (the metadata between the first pair of `---` lines) plus Markdown or MDX below for the long-form page.

**Blogs** are not wired up in this repo yet—only `projects/` exists for now.

---

## Adding a project

1. Create `projects/your-slug.mdx` (use a URL-friendly filename; it is often used as the page id on the site).
2. Copy the frontmatter block below and fill in the fields.
3. Write the page body under the closing `---` (headings, lists, links, etc.).

### Frontmatter reference

| Field | Required | Type / notes |
|--------|----------|--------------|
| `title` | yes | string — display name |
| `description` | yes | string — short blurb (cards, SEO, previews) |
| `tags` | yes | YAML array of strings, e.g. `[Astro, TypeScript]` |
| `status` | yes | `active`, `wip`, or `archived` |
| `year` | yes | number — e.g. `2026` |
| `month` | yes | integer `1`–`12` |
| `thumbnail` | no | string — full URL to preview image |
| `links` | no | object; keys are optional (see below) |
| `links.github` | no | full URL to the repository |
| `links.live` | no | full URL to the deployed site |
| `featured` | no | boolean; default `false` if omitted |
| `order` | no | number; lower sorts first; default `999` if omitted |

### Minimal example

```yaml
---
title: My project
description: One-line summary for listings and previews.
tags: [TypeScript, Vite]
status: wip
year: 2026
month: 5
---
```

### Example with optional fields

```yaml
---
title: My project
description: One-line summary for listings and previews.
tags: [TypeScript, Vite]
status: active
year: 2026
month: 5
featured: true
order: 1
thumbnail: https://example.com/card.png
links:
  github: https://github.com/you/repo
  live: https://your-project.example.com
---

## Why

Your narrative starts here.

## Stack

- **Vite** — …
```
