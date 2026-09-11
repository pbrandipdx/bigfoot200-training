# Bigfoot 200 — training site

**https://pbrandipdx.github.io/bigfoot200-training/**

Four pages: **Today** (this week's schedule and next race), **Log** (weekly Strava
rollups and charts), **Blocks** (block targets and monitors), **Race plan** (the
97:00 pacing schedule).

## Rebuilds itself

A GitHub Action (`.github/workflows/rebuild.yml`) clones `pbrandipdx/bigfoot-200`,
runs its build, and commits any change here — every 15 minutes, and on demand via
the **Run workflow** button on the Actions tab.

So you can edit `plan/schedule.json` or the plan markdown in the GitHub web editor,
from any device, and the live site catches up within 15 minutes. No Mac required.
`make sync` on a Mac is still the fast path — it publishes immediately.

No secrets are involved: `bigfoot-200` is public so cloning needs no auth, and the
built-in `GITHUB_TOKEN` pushes here.

## This repo is generated — do not edit it

Every `.html` file here is overwritten by `make dashboard` in the private
`pbrandipdx/bigfoot-200` repo. Edits made here are erased on the next build.

To change something, edit the source in `bigfoot-200`:

| To change | Edit |
|---|---|
| Block dates, targets, race ladder | `plan/schedule.json` (and the prose in `plan/block-targets.md`) |
| Block detail page | `plan/block-targets.md` |
| Race plan page | `plan/sub100-plan.md` |
| Training data | `tracker/weeks.json` (weekly Strava refresh) |
| Page layout | `dashboard/template.html`, `tracker/template.html`, `dashboard/doc_shell.py` |

then `make dashboard`, and commit here.

The official Destination Trail runner manual is **not** published here — it's
copyrighted and stays in the private repo.
