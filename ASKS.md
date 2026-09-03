# ASKS — presentation

## A1 · A merge that adds a root file or a seat needs something that checks the README still agrees with it

`status: draft` · `source: simulated` · `first said: 2026-09-03` · `target: this repository`

Whoever reviews a PR that touches `advocate.yml` or adds a file at the repo root needs a way to
notice, before merging, that `README.md` and `AGENTS.md`'s orientation table still match what's
there — a seat count, a new root file, a new mounted engine. Not a person assigned to remember it;
a shape that surfaces the mismatch at the point a human is already looking, the way a PR template
checklist item or a CI check on file-count-vs-README-mentions would. One data point so far (C2)
isn't enough to know if this should be automated or just asked for — filing it now so it isn't
re-derived next time the same gap shows up.
