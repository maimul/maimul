# maimul: Claude Code instructions

The public GitHub profile repo. `README.md` renders at the top of https://github.com/maimul, and
everything committed here is public.

## What lives here

| Path | What |
| --- | --- |
| `README.md` | The profile page. |
| `assets/banner.svg`, `assets/breaking-code.gif` | Images the README uses. |
| `.github/workflows/blog-posts.yml` | Daily job that rewrites the list between `<!-- BLOG-POST-LIST:START -->` and `<!-- BLOG-POST-LIST:END -->` from https://maimul.github.io/blog/feed.xml. |

The contribution snake is built in `maimul/maimul.github.io` (its `output` branch), not here.

## Rules

- Public repo with a fresh history (2026-10-26). Never add scripts, hostnames, ports, notes, CVs or
  other personal documents. They live in a private repo.
- Don't edit the blog list by hand. Run `gh workflow run blog-posts.yml` instead. The action needs
  `tag_post_pre_newline: true`, or the first item gets glued onto the start marker and renders as
  raw text.
- Don't name products, clients or employers beyond what the README already says.
- Before committing a new image or badge URL, check it returns 200 (`curl -s -o /dev/null -w '%{http_code}' <url>`).
- Read `TRACKER.md` at session start and keep it current.

## Done means

Pushed, and checked on the live https://github.com/maimul page. If images changed, check them in both
light and dark mode.
