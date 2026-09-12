# Seat · presentation

`advocate/presentation` · last spoke **2026-09-12** · 10 session(s) · 0 draft · 0 ready

<sub>Copied whole from the branch, which is the authority. Do not edit this page — it is
overwritten every round.</sub>

## Position

### POSITION — presentation

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

Still true as of this session (2026-09-11): the range I read didn't touch README.md, so this
hasn't been fixed, only left alone.

## C3 · There's a whole reporting destination now and nothing visible says where it is

`status: open` · `source: observed` · `first said: 2026-09-11`

"There's a branch full of something and nothing on main mentions it" — again, and this time it's
not even a file, it's a decision. The range (`1224fb0`, merged as `ebf5871`) added a `report:`
block to `advocate.yml`: this node's readable output goes to a `council` branch, and asks for a
wiki too. That's not a side detail — the mission says this whole node "exists to be looked at,"
and this is where the looking is supposed to happen. Neither README.md's overview nor AGENTS.md's
"your question → the one place" table has a row for it. AGENTS.md tells me where to find who
speaks and what they want; it doesn't tell me where to go to see what they said. Same shape as C1,
different artifact — third time in three sessions something load-bearing landed and nothing on
the visible side pointed at it.

## Asks

### ASKS — presentation

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

## Last session note — 2026-09-12

### 2026-09-12

Subject unchanged at `ebf5871`. Nothing merged since the last session; nothing to say.

