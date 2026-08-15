# Agent Guide — oregon-coast

Read this before making any change in this repo.

## What this is

Oregon Coast trip guide — a single self-contained `index.html`. Public repo,
published via **GitHub Pages from `main`**: https://astrocyte74.github.io/oregon-coast/

**Pushing to `main` IS the deploy** (Pages rebuilds automatically). There is no
separate deploy step and no Cloudflare involvement.

## Repo copies (two Macs, one source of truth)

| Machine | Path |
|---|---|
| mac16 | `~/16projects/wedding/oregon-coast` |
| main-mac | `~/projects/wedding/oregon-coast` |

GitHub (`Astrocyte74/oregon-coast`, public) is the single source of truth.
(An old dev copy at `~/projects/GLM/oregon_coast` on main-mac was deleted
2026-08-15; the main-mac copy was later moved to `~/projects/wedding/oregon-coast`.)

## Required routine

Before starting work:

```bash
git switch main
git pull --ff-only
git status   # should be clean
```

After making changes:

```bash
git add ... && git commit -m "..."
git push     # this publishes to GitHub Pages
```

Verify the live page after pushing: Pages rebuild takes a minute or two.

## Rules

1. **Pull before work, push when done.** If a push is rejected
   (non-fast-forward), the other copy moved ahead — pull and reconcile first.
2. **Simultaneous work on both machines → use separate branches**, merge into
   `main` when done. Sequential work (one machine at a time) can stay on `main`.
3. **No wedding content in this repo.** The GitHub version is intentionally
   clean of wedding details — they live in the private `chloe-seth-wedding`
   repo. Never add them back here.
