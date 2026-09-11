# Bigfoot 200 — training site

**https://pbrandipdx.github.io/bigfoot200-training/**

Four pages: **Today** (this week's schedule and next race), **Log** (weekly Strava
rollups and charts), **Blocks** (block targets and monitors), **Race plan** (the
97:00 pacing schedule).

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
