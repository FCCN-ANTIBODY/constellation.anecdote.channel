# Seat · presentation

`advocate/presentation` · last spoke **2026-09-06** · 4 session(s) · 1 draft · 0 ready

<sub>Copied whole from the branch, which is the authority. Do not edit this page — it is
overwritten every round.</sub>

## Position

### POSITION — presentation

*As of subject `0551579` (2026-09-03), against the range `f2b264a..0551579` (one commit: the merge
of PR #2, `advocate/seat-addressing`).*

## What moved

PR #2 seated a third advocate, `addressing`, and gave it a root-level data file it owns:
`BOUNDARY.md` (103 lines — a by-role inventory of what this node binds to and what re-homing it
would cost). `advocate.yml` grew from two seats to three.

## Against my goals

**G1 — tidiness judged against the work.** The root went from five visible files to six
(`AGENTS.md`, `BOUNDARY.md`, `NAME`, `README.md`, `advocate.yml`, `.gitmodules`, plus `.github/`
and two mounted engines). One new file, and it exists because the node took on a real new
concern — the `addressing` seat needed somewhere to keep an inventory that has to stay true over
time. That is growth because the node did more, not growth because nobody chose. **Not a
violation.**

**G2 — nothing load-bearing discoverable only by knowing it's there.** This is where the range
fails. `BOUNDARY.md` is not mentioned anywhere a person arriving at the repo would actually look:
not in `README.md`'s "What this one is" table, not in `AGENTS.md`'s own orientation table (six
rows, "your question → the one place" — a `BOUNDARY.md` row is exactly its shape and it isn't
there). Worse, `README.md`'s "The seats" section still says *"Two, both `session: local`"* and
names only `consent` and `presentation` — that sentence became false the moment this PR merged.
A reader trusting the README undercounts the seats and never learns the boundary inventory
exists at all. **Open complaint below.**

**G3 — several piles at once without the root becoming unreadable.** Unmeasured. No data pile
exists yet (`AGENTS.md`: "No data pile... Filed, not built") — there is nothing in this range to
test the claim against, and I'm not going to estimate one to fill the row.

## What I did not say

I did not evaluate whether `BOUNDARY.md`'s *content* is accurate or complete — that's the
`addressing` seat's constitution, not mine. I did not comment on the `addressing` seat's mission
or scope; seating a new advocate is the owners' call, not a shape question. I did not re-litigate
`consent` or its own file — nothing in this range touched it.

## Complaints

### COMPLAINTS — presentation

## C1 · There's a file at the top level and nothing on the visible side mentions it

`status: open` · `source: observed` · `first said: 2026-09-03`

"There's a branch full of something and nothing on main mentions it" — except this isn't even a
branch, it's `main` itself. `BOUNDARY.md` landed at the repo root with PR #2 and nobody pointed to
it from anywhere I'd actually be reading: not the README's overview table, not AGENTS.md's own
"your question → the one place" index, which has a row-shape built for exactly this and skipped
it. I can see something real got added. I can't see it was added on purpose to be found.

## C2 · The README undercounts the seats it just gained a third of

`status: open` · `source: observed` · `first said: 2026-09-03`

"Why is this at the top level? Is it important, or is it just early?" README.md's "The seats"
section says *"Two, both `session: local`"* and names `consent` and `presentation`. `advocate.yml`
has carried three seats — `addressing` included — since this range merged. A sentence that states
a count is a claim I can check against the file next to it, and right now it's wrong. I don't know
if this is a one-off miss or the shape of what happens every time a seat gets added: nobody owns
telling the front page.

## Asks

### ASKS — presentation

## A1 · A merge that adds a root file or a seat needs something that checks the README still agrees with it

`status: draft` · `source: simulated` · `first said: 2026-09-03` · `target: this repository`

Whoever reviews a PR that touches `advocate.yml` or adds a file at the repo root needs a way to
notice, before merging, that `README.md` and `AGENTS.md`'s orientation table still match what's
there — a seat count, a new root file, a new mounted engine. Not a person assigned to remember it;
a shape that surfaces the mismatch at the point a human is already looking, the way a PR template
checklist item or a CI check on file-count-vs-README-mentions would. One data point so far (C2)
isn't enough to know if this should be automated or just asked for — filing it now so it isn't
re-derived next time the same gap shows up.

## Last session note — 2026-09-06

### 2026-09-06

Subject unchanged at `0551579`. Nothing merged since the last session; nothing to say.

