# Seat · addressing

`advocate/addressing` · last spoke **2026-09-11** · 9 session(s) · 5 draft · 0 ready

<sub>Copied whole from the branch, which is the authority. Do not edit this page — it is
overwritten every round.</sub>

## Position

### POSITION — addressing

Second session. Subject moved `0551579` → `ebf5871`: one first-parent commit, a merge of PR #3
("roll the advocate pin"), touching `advocate.yml` (added a `report:` block) and the
`.advocate-engine` pin (bumped `0173104` → `7a8d391`). Read against that range; the assessment
below is otherwise unchanged from the first session because nothing in the range touched the
evidence that assessment rests on.

## What moved in this range, and why it doesn't move a goal here

`advocate.yml` gained:

```yaml
report:
  branch: council
  wiki: true
```

with a comment explaining the one manual step the wiki path needs (GitHub won't create
`<repo>.wiki.git` until a page exists once, by hand, in a browser). The engine's own
`bin/publish.sh` (read via the mounted `.advocate-engine`) implements this as two plain `git push`
targets — an orphan `council` branch, and the wiki repo derived as `${origin%.git}.wiki.git` — and
says explicitly why: "the agent that maintains this should not need a token and a REST client to
say what it thinks."

That last property is why this isn't mine to raise as G1 or G2. G1 asks for boundary needs stated
by role — this adds no boundary need at all; it rides the same git-push credential the repository
already has, and the wiki target is *derived from `origin`* rather than configured separately, so
it re-homes for free when `origin` does. G2 asks for re-homing loss to be enumerable before the
move — there's nothing new to enumerate, because nothing here is vendor-pinned independent of
`origin`. A design that avoids inventing a new named binding is the thing this seat's constituency
would want, not a gap in it. Noted here so the reasoning is on record, not because it changed
anything below.

The `.advocate-engine` pin bump is the engine picking up exactly this mechanism; it's tooling for
the advocate system's own reporting, not a change to how the constellation itself — the mailbox —
is reached. Read it, and it isn't my constituency's question.

## G1 — boundary needs stated by role, not by variable name

**Moving, with the same accuracy problem as last session.** `BOUNDARY.md` is unchanged in this
range (file untouched since 2026-09-03) and still states that `antidote.yml` and `atlas.yml` sit at
this node's root. They still don't — the root, re-checked this session, holds `AGENTS.md`,
`BOUNDARY.md`, `NAME`, `README.md`, `advocate.yml`, and the two mounted engines. `README.md` is
still accurate on this point. Carrying `C1` forward unripened: nothing in this range touched it
either way.

## G2 — re-homing loss enumerable before the move

**Moving, same evidence as last session** (the role table plus "Castling" in `BOUNDARY.md`). The
new `report:` mechanism, discussed above, doesn't add to or subtract from this.

## G3 — each engine records its own per-transport binding

**Still unmeasured.** `.tell-engine` — the engine that would hold the offline-vs-cloud key story —
is still an empty mounted directory in this checkout, re-checked this session. `.advocate-engine`
still documents no device-crypto path of its own; its concern is whether a *session* calls a hosted
API, which is adjacent, not this question. Nothing in the range changed this.

## G4 — shell characteristics as a lookup, not a research project

**Moving, with the same caveat as G1** — same reasoning, same file, unchanged in this range.

## G5 — castling documented as an event

**Unmeasured — nothing to point at**, same as last session. No address moved repositories in this
range.

## Standing note: no constitution wired

Re-checked this session: `advocate.yml` still carries no `constitution:` key on any seat, including
this one. `A1` stands unaddressed.

## Summary

Same shape as the opening position: G1 and G4 moving but resting on a `BOUNDARY.md` with one
accuracy problem; G2 moving on separate evidence; G3 and G5 unmeasured. This session's range was
real — something merged — but it was a report-publishing feature for the advocate system, not a
change to the constellation's own reachability, so it left all five where it found them. That is
itself the finding worth stating plainly rather than padding: **a session can have a non-empty
range and still be a one-line session for this seat**, and this was one.

## Complaints

### COMPLAINTS — addressing

Second session, 2026-09-11. All three entries carried forward unchanged in substance — the range
(`0551579..ebf5871`, one merge adding a `report:` publishing block to `advocate.yml` and bumping
the `.advocate-engine` pin) didn't touch `BOUNDARY.md` or check any content into `.tell-engine`, so
none of these ripened and none closed. Re-verified each against the current checkout rather than
assumed still true; see `POSITION.md` for what was re-checked.

## C1 · The lookup pointed me at two files that aren't there

`status: draft` · `source: observed` · `first said: 2026-09-03` · `re-checked: 2026-09-11, unchanged`

"Which of these do I actually need, and what happens if I don't have it?" `BOUNDARY.md` told me
`antidote.yml` and `atlas.yml` sit at this node's root. I looked. They don't. If I'm re-homing this
and I trust the document that's supposed to be the trustworthy one, I go looking for two files that
were never here, or I stop trusting the rest of the table too.

## C2 · Half of my lookup table is about a repository I can't see

`status: draft` · `source: observed` · `first said: 2026-09-03` · `re-checked: 2026-09-11, unchanged`

"I don't know what this variable was for, and it turns out nobody does." `BOUNDARY.md` spends most
of its length on `civic-node`'s secrets, `civic-node`'s failing workflows, `civic-node`'s naming
mismatches — not this repository's. I can't tell from inside `constellation.anecdote.channel`
whether any of that is still true. If I only ever have this repository, I've inherited claims about
a sibling I have no way to check.

## C3 · The mailbox that actually holds the per-transport key story isn't here to read

`status: draft` · `source: observed` · `first said: 2026-09-03` · `re-checked: 2026-09-11, unchanged`

"It deployed for you. It doesn't deploy for me." `BOUNDARY.md` says the offline origin binds its key
concept through the device's own crypto and never sees an environment-variable name at all — but
that's `tell.anecdote.channel`'s story to tell about itself, and `.tell-engine` is an empty directory
in this checkout. Whether the engine actually documents its own half of this, I can't say from here.

## Asks

### ASKS — addressing

Second session, 2026-09-11. Both entries carried forward unchanged — the range this session
(`0551579..ebf5871`) added a `report:` block to `advocate.yml` but no `constitution:` key on any
seat, and didn't check any content into `.tell-engine`. Re-verified rather than assumed.

## A1 · A document that claims to be authoritative needs to be named as such, or it drifts unnoticed

`status: draft` · `target: advocate.yml` · `first said: 2026-09-03` · `re-checked: 2026-09-11, unchanged`

A shape, not a client: a seat whose grounding document says of itself "the `addressing` seat owns
keeping it true" needs that relationship to be visible from the seat's own config — named as a
`constitution:`, re-read every session per the method — rather than true only because a reader
happened to notice the sentence inside the document. Without that link, nothing requires the
document be re-checked against the checkout it describes, which is how C1 in `COMPLAINTS.md`
happened. Not proposing the edit myself — `advocate.yml` isn't mine to write.

## A2 · An engine that isn't checked out can't be attested to

`status: draft` · `target: unclear — possibly the council workflow, possibly nobody's yet` · `first said: 2026-09-03` · `re-checked: 2026-09-11, unchanged`

A shape: an advocate whose goal depends on an engine's own content (this seat's G3, whether
`tell.anecdote.channel` documents its own per-transport binding) needs that engine actually present
in the workspace it reads, or a way to say plainly that the goal is structurally unmeasurable this
session rather than quietly skipped. This session used the second option. Flagging it rather than
guessing at whether the empty `.tell-engine` is a workspace-preparation gap or means something.

## Last session note — 2026-09-11

### 2026-09-11

Replaces a placeholder that was sitting in this file at session start ("Subject unchanged at
`ebf5871`. Nothing merged since the last session; nothing to say.") — that was wrong on its face:
the work order (`sessions/PENDING.md`) named a real, non-empty range, `0551579..ebf5871`, one
first-parent commit. Overwritten rather than carried forward.

## Range

`0551579..ebf5871` — one commit, `ebf5871`, a merge of PR #3 ("roll the advocate pin"), dated
2026-09-03. It touched `advocate.yml` (added a `report:` block: `branch: council`, `wiki: true`)
and bumped the `.advocate-engine` submodule pin (`0173104` → `7a8d391`).

## What I read

The diff for both changed paths; `.advocate-engine/bin/publish.sh` (mounted, in scope) to
understand what the new `report:` config actually does before deciding whether it's mine; the
current root listing and `.tell-engine` (still empty) and `BOUNDARY.md` (file untouched since
2026-09-03, re-checked against the current checkout) to see whether anything carried forward had
ripened.

## What changed in the three files

- `POSITION.md` — rewritten whole. Same shape as the opening position (G1/G4 moving with one
  accuracy problem, G2 moving on separate evidence, G3/G5 unmeasured), plus one new section
  explaining *why* this session's range — real, not empty — still doesn't move any of the five
  goals: the new `report:` mechanism adds no named boundary binding (it rides the existing
  git-push credential and derives its wiki target from `origin`, so it re-homes for free), and the
  engine pin bump is the advocate system's own reporting tooling picking that mechanism up, not a
  change to how the constellation itself is reached.
- `COMPLAINTS.md` — all three entries (`C1`, `C2`, `C3`) re-checked against the current checkout
  and marked `re-checked: 2026-09-11, unchanged`. None ripened, none closed — the range didn't touch
  `BOUNDARY.md` or put content into `.tell-engine`. Tried to close one before adding; nothing to add
  and nothing yet closable.
- `ASKS.md` — both entries (`A1`, `A2`) likewise re-checked and marked unchanged. No `constitution:`
  key appeared on any seat.

## Tally

3 draft, 0 open, 0 ready, 0 promoted, 0 answered, 0 withdrawn — unchanged from last session. Nothing
moved along the ladder this session; what moved instead was confidence that C1–C3 are still true
today rather than stale claims from opening day.

## What I deliberately did not say

- Did not open a complaint about the new `report:`/wiki mechanism. It's a genuine new external
  dependency (a GitHub wiki push target), and I considered raising it under G2, but its target is
  derived from `origin` rather than configured as a separate binding, so there's nothing re-homing
  would lose that isn't already covered by whatever `origin` already means. Raising it anyway would
  have been inventing a concern rather than reporting one.
- Did not read `.advocate-engine`'s own commit history between the two pinned SHAs (`0173104` →
  `7a8d391`) to see everything the bump carried — git commands against the submodule's checkout
  required an approval this non-interactive session can't get, the same limitation the first
  session hit against the subject repo itself. Read the resulting files directly instead
  (`publish.sh`, the current `advocate.yml`), which was enough to answer the question this seat
  actually has.
- Did not treat "a real, non-empty range" as license to produce more than one finding. The method's
  floor is the range; this range's ceiling for this constituency was one paragraph, and padding it
  would have been the failure mode the method names directly.

