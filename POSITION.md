# POSITION — addressing

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
