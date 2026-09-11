# POSITION — presentation

*As of subject `ebf5871` (merged 2026-09-03, session run 2026-09-11 — a work order that sat unrun),
against the range `0551579..ebf5871` (two commits: `1224fb0` "Roll the advocate pin, and ask for the
wiki", merged as `ebf5871`).*

## What moved

The range bumps `.advocate-engine`'s pin (`0173104` → `7a8d391`) and adds a `report:` block to
`advocate.yml`: the council's readable output now has a stated destination, a `council` branch
(already working) and a requested wiki (needs a manual first-page save before it exists; the
commit message says so and `publish.sh` will keep saying so until someone does it).

## Against my goals

**G1 — tidiness judged against the work.** No new root file. `advocate.yml` grew by twelve lines
inside itself, and the submodule pin move is a one-line diff on a file that's already there. Root
file count: unchanged. **Not a violation** — this is the node doing more, recorded where the doing
already lives.

**G2 — nothing load-bearing discoverable only by knowing it's there.** This is where the range
fails, again. The `report:` block decides where this node's entire readable output goes — and the
mission line is literally "it exists to be looked at." Neither README.md's overview nor AGENTS.md's
orientation table gets a row for it. AGENTS.md tells a reader where to find who speaks and what they
want; it has nothing telling them where to go see what was said. Filed as C3 — same shape as C1
(`BOUNDARY.md`, 2026-09-03), different artifact. Two sessions, two unrelated merges, same failure:
that's no longer a one-off, so I moved A1 from `draft` to `open`.

**G3 — several piles at once without the root becoming unreadable.** Still unmeasured. Still no data
pile to test it against.

## Where my items stand

- Complaints: C1 `open`, C2 `open` (still true — this range didn't touch README, so nothing closed
  it), C3 `open` (new).
- Asks: A1 `open` (moved from `draft` — two data points now, not one).
- Nothing closed this session. Nothing was in a state where closing it would have been honest.

## What I did not say

I did not evaluate the `.advocate-engine` pin bump itself — what changed inside that engine, whether
rolling it was correct, whether the three bugs its commit message names are real fixes. That's the
engine's own internals, out of scope for this seat by name. I did not evaluate whether routing the
council's report through a branch-plus-wiki is a *good* mechanism, or whether the wiki's manual
bootstrap step is a real problem — that reads closer to reachability than to shape, and it isn't
mine to take on just because I noticed it. I did not re-litigate C1 or C2; nothing in this range
touched them, so there's nothing new to say about either beyond "still true."
