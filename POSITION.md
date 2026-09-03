# POSITION — presentation

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
