# POSITION — presentation

*As of subject `1e5ee75` (2026-09-11), against the range `ebf5871..1e5ee75`: PR #4
"mail-that-cannot-be-delivered" (`12d664f`) and PR #5 "bump-engine-for-mail" (`1e5ee75`).*

## What moved

PR #4 puts `MAIL.md` at the repo root: a survey of 22 filed petitions and why none can reach a
seat. PR #5 rolls the `.advocate-engine` pin so this node can receive mail. I did not read the
diffs themselves; I read the tree as it stands.

## Against my goals

**G1 — tidiness judged against the work.** One new root file. It is a survey of what the node is
now doing (mail delivery across repositories), so the growth was chosen. **Not a violation.**

**G2 — nothing load-bearing discoverable only by knowing it's there.** Fails a fourth time.
`MAIL.md` says of itself that no seat owns it. `README.md` and `AGENTS.md` don't mention it, and
neither mentions `BOUNDARY.md` or the `report:` destination. `AGENTS.md`'s table is still the
one from before those landed. Also still stale: README says the node has "Two" seats and
`AGENTS.md` says "Both seats are drafts"; `advocate.yml` holds three. C1, C2, C3 stand; C4 added.

**G3 — several piles at once.** `unmeasured`. There is still no pile here to test against.

## Where my items stand

- Complaints: C1 `open`, C2 `open`, C3 `open`, C4 `draft` (new).
- Asks: A1 `open` — now four data points, same shape.
- Nothing closed. Nothing had changed that would make closing honest.

## What I did not say

`MAIL.md` names `presentation` as "the closest existing constituency" and asks who should hold it.
That is the owners' call to make by seating, not mine to claim; I have not taken it, and its
contents (delivery gates, pin state, rounds) are not my subject. I did not judge the pin bump.
