---
title: iPhone-readable brief pages on a stable URL
slug: 0001-iphone-html-pages
status: in-progress
owner: jadecli
created: 2026-05-21
---

## Why

The operator works from iPhone Chrome (claude.ai web, not the mobile app).
Briefs need to live somewhere durable, share-able with one tap, and readable
without horizontal scroll. Chat scrollback is not durable. Notion is not
git-versioned. A static markdown-rendered worker is.

## Outcome

`https://subagentbriefs.<account>.workers.dev/0001-iphone-html-pages`
renders this file as clean HTML on iPhone Chrome.
The operator taps a link from a claude.ai chat → reads the brief → has
context. No IDE, no app install, no auth.

## Acceptance

1. Every file in `briefs/*.md` is reachable at `/<slug>` on the worker
2. Frontmatter validates: title, slug, status, owner, created all present
3. The page fits iPhone Chrome's viewport without horizontal scroll
4. No JavaScript is required to read the brief
5. `cmark --to commonmark` round-trips every brief in CI
6. Internal links between briefs work
7. Worker cold-start under 200ms on warmed edge

## Non-goals

- Not building a CMS or admin UI
- Not styling-rich — minimal sans-serif default is fine
- Not handling auth — everything public
- Not search across briefs (use git grep + GitHub)
- Not generating briefs from Hamster docs

## Working backwards

```
END        operator opens link on iPhone, brief renders cleanly
                              ↑
deploy     worker live at subagentbriefs.<account>.workers.dev
                              ↑
worker     code in render/ that does md → HTML at /<slug>
                              ↑
ci         normalize-and-validate workflow on every push
                              ↑
schema     frontmatter schema enforced
                              ↑
seed       this brief + _template.md + the PRD
                              ↑
START      this commit
```

## Out of band

The 5,981-file `knowledge-engineering/` chassis was vendored on
2026-05-21 from `subagentceo/knowledge-engineering`. Git history was
removed. Treat it as read-only.

The 323-page Hamster crawl in `discovery/hamster/` is informational
reference. Do not link from briefs.
