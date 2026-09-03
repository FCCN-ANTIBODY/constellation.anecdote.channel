# Seat · addressing

`advocate/addressing` · last spoke **2026-09-03** · 1 session(s) · 5 draft · 0 ready

<sub>Copied whole from the branch, which is the authority. Do not edit this page — it is
overwritten every round.</sub>

## Position

### POSITION — addressing

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

## Complaints

### COMPLAINTS — addressing

First session. Nothing carried forward — this file was empty. Every entry below is new, opened
against the repository as read, never against a change (there is no range yet).

## C1 · The lookup pointed me at two files that aren't there

`status: draft` · `source: observed` · `first said: 2026-09-03`

"Which of these do I actually need, and what happens if I don't have it?" `BOUNDARY.md` told me
`antidote.yml` and `atlas.yml` sit at this node's root. I looked. They don't. If I'm re-homing this
and I trust the document that's supposed to be the trustworthy one, I go looking for two files that
were never here, or I stop trusting the rest of the table too.

## C2 · Half of my lookup table is about a repository I can't see

`status: draft` · `source: observed` · `first said: 2026-09-03`

"I don't know what this variable was for, and it turns out nobody does." `BOUNDARY.md` spends most
of its length on `civic-node`'s secrets, `civic-node`'s failing workflows, `civic-node`'s naming
mismatches — not this repository's. I can't tell from inside `constellation.anecdote.channel`
whether any of that is still true. If I only ever have this repository, I've inherited claims about
a sibling I have no way to check.

## C3 · The mailbox that actually holds the per-transport key story isn't here to read

`status: draft` · `source: observed` · `first said: 2026-09-03`

"It deployed for you. It doesn't deploy for me." `BOUNDARY.md` says the offline origin binds its key
concept through the device's own crypto and never sees an environment-variable name at all — but
that's `tell.anecdote.channel`'s story to tell about itself, and `.tell-engine` is an empty directory
in this checkout. Whether the engine actually documents its own half of this, I can't say from here.

## Asks

### ASKS — addressing

First session. Nothing carried forward — this file was empty.

## A1 · A document that claims to be authoritative needs to be named as such, or it drifts unnoticed

`status: draft` · `target: advocate.yml` · `first said: 2026-09-03`

A shape, not a client: a seat whose grounding document says of itself "the `addressing` seat owns
keeping it true" needs that relationship to be visible from the seat's own config — named as a
`constitution:`, re-read every session per the method — rather than true only because a reader
happened to notice the sentence inside the document. Without that link, nothing requires the
document be re-checked against the checkout it describes, which is how C1 in `COMPLAINTS.md`
happened. Not proposing the edit myself — `advocate.yml` isn't mine to write.

## A2 · An engine that isn't checked out can't be attested to

`status: draft` · `target: unclear — possibly the council workflow, possibly nobody's yet` · `first said: 2026-09-03`

A shape: an advocate whose goal depends on an engine's own content (this seat's G3, whether
`tell.anecdote.channel` documents its own per-transport binding) needs that engine actually present
in the workspace it reads, or a way to say plainly that the goal is structurally unmeasurable this
session rather than quietly skipped. This session used the second option. Flagging it rather than
guessing at whether the empty `.tell-engine` is a workspace-preparation gap or means something.

## Last session note — 2026-09-03

### 2026-09-03 — first session

**Seated, not reporting.** `PENDING.md` named `first: true`, `range: null` — there is no baseline
yet, so there is nothing to diff against. This session read the repository as it stands at
`0551579` and formed an opening `POSITION.md` against the five goals in `advocate.yml`.

Replaces a placeholder session note that was already sitting in this file at session start
(`"Nothing merged since the last session; nothing to say."`) — that line assumed a range that
does not exist for a first session, so it was wrong on its face and is overwritten rather than
carried forward.

## What I read

`README.md`, `AGENTS.md`, `BOUNDARY.md`, `advocate.yml`, `NAME`, `.gitmodules`,
`.github/workflows/council.yml`, `.advocate-engine/{LOCAL.md,STATUS.md}`, and the root directory
listing. `.tell-engine` is a mounted submodule with no content checked out — noted, not chased;
reading `tell.anecdote.channel` directly would be a repository not in this checkout. `civic-node`,
which `BOUNDARY.md` describes at length, is likewise not in this checkout and was not read.

## What changed

- `POSITION.md` — written whole, first time. G1 and G4 moving (`BOUNDARY.md` exists, is dated
  today, and does the by-role framing G1 asks for) but with an accuracy problem in that same
  document: it claims `antidote.yml` and `atlas.yml` sit at this root, and they don't. G2 moving on
  the same evidence. G3 and G5 reported `unmeasured`, for different reasons each.
- `COMPLAINTS.md` — three opened, all `draft`, all `source: observed`. None are testimony; nobody
  relayed anything to this seat yet.
- `ASKS.md` — two opened, both `draft`. Neither proposes an edit to `advocate.yml` — that file
  isn't mine to write, so A1 names the gap and stops there.

## Tally

3 draft, 0 open, 0 ready, 0 promoted, 0 answered, 0 withdrawn — across both files. Nothing to move
yet; this is the session that creates the first thing to move.

## What I deliberately did not say

- Did not treat the `antidote.yml`/`atlas.yml` discrepancy as a verdict on which document is wrong.
  I don't have git history in this checkout (git access to the subject repo required approval this
  non-interactive session couldn't get), so I can't say whether those files existed and were
  removed, or were never there. Recorded only what the checkout currently shows against what
  `BOUNDARY.md` currently claims.
- Did not read or guess at `civic-node`'s actual state to check `BOUNDARY.md`'s claims about it
  (the failing `antidote-heartbeat.yml`, the absent `ATLAS_SIGNER_KEY`, and so on). Those may be
  exactly right. Confirming them would mean reading a repository not in this checkout, which the
  method refuses.
- Did not propose that `advocate.yml` name `BOUNDARY.md` as this seat's constitution, only noted
  that no seat has one and that the absence is the method's own first finding. Wiring it is a
  decision for whoever owns that file.
- Did not write complaints about `presentation`'s or `consent`'s territory (the empty data pile,
  the absent Atlas) even where `BOUNDARY.md` and `README.md` touch on them — not this
  constituency's question.

