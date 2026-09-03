# POSITION — addressing

Opening position. First session — there is no range; this reads the repository as it stands
at `0551579` and states where it is against the five goals in `advocate.yml`. Nothing below is a
complaint about a change, because no change has been observed yet. It is a survey.

## G1 — boundary needs stated by role, not by variable name

**Moving.** `BOUNDARY.md` exists at this node's root, dated the same day as this seating, and states
plainly that it is owned by this seat ("The `addressing` seat in `advocate.yml` owns keeping it
true"). Its "Roles, not names" table is exactly the shape G1 asks for — publish, certificate, cache,
rules, zone identity, signing, cross-repo write — each with why it matters and who binds it, not
just a secret's name.

**But it is not accurate about this repository right now.** It states "`antidote.yml` and
`atlas.yml` sit at this node's root" — neither file exists at this checkout's root. The root holds
exactly: `AGENTS.md`, `BOUNDARY.md`, `NAME`, `README.md`, `advocate.yml`, plus the two mounted
engines. `README.md`, by contrast, is accurate here — it says plainly "No Atlas... Nothing is
scheduled" and lists only the two engines. So the document written to be the lookup table disagrees
with the document written to be the orientation, about the same root, on the same day. A person
re-homing this project and trusting `BOUNDARY.md` would go looking for two files that are not there.

**Also unverifiable from here:** much of `BOUNDARY.md`'s content is not about this repository at
all — it describes `civic-node`'s secrets, its failing `antidote-heartbeat.yml`, its
`ATLAS_SIGNER_KEY`. `civic-node` is not in this checkout, so I cannot confirm or dispute any of
that half of the document. It may be exactly right. It is a claim this seat cannot audit without
widening scope, which the method refuses.

## G2 — re-homing loss enumerable before the move

**Moving, on the same evidence.** The role table plus the "Castling" section are precisely an
enumeration-before-the-move. `BOUNDARY.md` calls itself "incomplete on purpose, in the `draft`
sense" — an honest label. No castling has happened yet to test the claim against (see G5).

## G3 — each engine records its own per-transport binding

**Unmeasured.** `BOUNDARY.md` states the general principle (cloud env var vs. the offline origin's
own device crypto, both required to be up at once) but G3 asks whether *each engine* records this
for itself. `.advocate-engine` is mounted and readable; nothing in it documents a device-crypto path
— its own `LOCAL.md` is about whether a *session* calls a hosted API at all, which is an adjacent
question, not this one. `.tell-engine` — the engine that actually holds the offline-vs-cloud key
question, since it's the mailbox — is mounted but **empty**: the submodule has no content checked
out in this workspace. I can't read what I don't have, and reading `tell.anecdote.channel` directly
would be a repository not in this checkout. Reporting `unmeasured` rather than guessing.

## G4 — shell characteristics as a lookup, not a research project

**Moving, with the same caveat as G1.** `BOUNDARY.md` is the lookup. A lookup with a row that
doesn't match the checkout is worse than no lookup, in the specific way this seat's constituency
described it: it's the difference between "I don't know what this variable was for" (this seat's own
voice line) and being confidently pointed at a file that isn't there.

## G5 — castling documented as an event

**Unmeasured — nothing to point at.** No address has moved repositories in this checkout's
visible history. The principle is written down in `BOUNDARY.md`; it hasn't been exercised.

## Standing note: no constitution wired

Per `METHOD.md` step 2: this seat's `advocate.yml` entry carries no `constitution:` key, and neither
does any other seat's. There is no sub-constitution to re-read. That is not a blocker, but the method
says the absence is itself a first finding, so it's recorded here rather than silently accepted.
`BOUNDARY.md` reads like it wants to be this seat's constitution — it says the seat owns keeping it
true — but nothing in `advocate.yml` names it as one, so nothing requires it be re-read, versioned,
or treated as binding rather than as one more file that can drift.

## Summary

Two goals (G1, G4) have real, recent work behind them and one accuracy problem in that same work.
One goal (G2) has real work behind it and no reason yet to distrust it. Two goals (G3, G5) are
unmeasured, for different reasons — G3 because the evidence isn't checked out where I can read it,
G5 because the event it watches for hasn't happened.
