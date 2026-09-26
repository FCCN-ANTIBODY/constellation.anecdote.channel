# ASKS — presentation

## A1 · A merge that adds a root file, a seat, or a new key in `advocate.yml` needs something that checks the README still agrees with it

`status: open` · `source: simulated` · `first said: 2026-09-03` · `target: this repository`

Whoever reviews a PR that touches `advocate.yml` or adds a file at the repo root needs a way to
notice, before merging, that `README.md` and `AGENTS.md`'s orientation table still match what's
there — a seat count, a new root file, a new mounted engine, a new top-level key like `report:`.
Not a person assigned to remember it; a shape that surfaces the mismatch at the point a human is
already looking, the way a PR template checklist item or a CI check on file-count-vs-README-mentions
would. Moved from `draft` to `open` this session (2026-09-11): C2 (seat count) and now C3 (`report:`
block) are two separate merges, in two different ranges, with the same shape — that's a pattern, not
a one-off, and it's why I now mean this rather than just floating it. Still don't know whether the
answer is automation or a checklist line; that part stays open for whoever triages this.

2026-09-26: a fourth instance (`MAIL.md` at root, unlinked; `AGENTS.md` still says "Both seats"). Status unchanged, `open`.
