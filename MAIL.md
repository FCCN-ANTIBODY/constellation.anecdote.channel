# What is filed for whom, and why none of it can be delivered yet

A survey kept **by deliverability**, because a petition that nobody can receive is
indistinguishable from one nobody wrote.

Seeded 2026-09-10 from an actual survey of every checkout on `Autumns-iMac` rather than from
memory; incomplete on purpose, in the `draft` sense of [`STATUS.md`](.advocate-engine/STATUS.md).
**No seat owns this file yet** — see "Who should hold this" at the end.

## The one-line finding

**22 petitions are filed. 0 of them can reach a seat.** Not because the mechanism is missing —
it shipped on 2026-09-08 — but because nothing has picked it up, and three separate things have
to be true for an item to arrive.

## The mechanism exists and is not the problem

`advocate.anecdote.channel` merged **PR #11, `a-seat-checks-its-mail`**, on 2026-09-08. It adds
`bin/petitions.mjs`, `test/petitions.test.mjs`, and the `PETITIONS.md` step in `METHOD.md` and
`bin/round.sh`.

Its design is worth restating here, because it is the reason this is safe to switch on:

- **Mail is fetched in the mechanical half, before the agent wakes up**, and written into the
  workspace the seat already reads. `METHOD.md` forbids an advocate from reading a repository
  outside its checkout, and that refusal is load bearing — so the seat never goes looking.
  *Scope is not widened; the inbox is delivered.*
- **A seat may only propose.** For each unread item it either carries it into `COMPLAINTS.md` /
  `ASKS.md` at `status: draft`, says it belongs to another seat, or says it belongs to nobody.
  Declining is a complete answer.
- **A seat may not clear the ground.** Verbatim: *"You do not edit, move, or delete anything in
  the petition space… Adopting one is something you write on your own branch; clearing it from
  the ground is a person's act, at triage."*

**That is the control boundary already built.** Turning delivery on does not delegate any
decision; it produces drafts on branches for a person to read.

## Three gates, and every item is behind at least one

| gate | what it means | how it is fixed |
| --- | --- | --- |
| **pin** | the repo mounts `.advocate-engine` at a commit older than PR #11, so `petitions.mjs` is not in its checkout | a one-line pin bump, **by PR, by whoever owns the repo** |
| **seat** | the repo has no `.advocate-engine` and no `advocate.yml` — there is nobody to deliver to | a seat has to be opened; a real decision, not a chore |
| **round** | the repo is absent from `rounds.conf`, so the caretaker never visits it | one line in `station-node/library/harness/rounds.conf` |

The pin gate is deliberately not fixable from outside. The docket's own rule: *"A repository's own
pin is reported and never bumped… advancing that is a change to that repository, made in a pull
request by whoever owns it. The caretaker says what it sees and does not vote."*

## The survey

Engine tip at survey time: `41b6358`. Petition support entered at `b2bc0ee`.

| target | filed | mounts engine | pin | in `rounds.conf` | blocked by |
| --- | ---: | --- | --- | --- | --- |
| `FCCN-ANTIBODY/anecdote.channel` | 5 | **no** | — | yes | seat |
| `FCCN-ANTIBODY/advocate.anecdote.channel` | 4 | **no** | — | **no** | seat, round |
| `FCCN-ANTIBODY/constellation.anecdote.channel` | 4 | yes | `7a8d391` (−10) | yes | **pin only** |
| `FCCN-ANTIBODY/civic-node` | 3 | **no** | — | **no** | seat, round |
| `FCCN-ANTIBODY/data-pile` | 2 | yes | `0173104` (−24) | **no** | pin, round |
| `FCCN-ANTIBODY/library.anecdote.channel` | 2 | yes | `4635cfc` (−2) | **no** | pin, round |
| `FCCN-ANTIBODY/tell.anecdote.channel` | 1 | **no** | — | **no** | seat, round |
| `Chaevity/ablative` | 1 | yes | `4635cfc` (−2) | yes (`max=1`) | **pin only** |

Three further items were filed on 2026-09-10 into `library.anecdote.channel` (2) and `unplaced/`
(1), in a separate pull request against `station-node`. They do not change any conclusion here.

### Two observations that are not table rows

**The engine cannot receive its own mail.** `advocate.anecdote.channel` has four petitions filed
against it, no `advocate.yml`, and does not mount itself. The repository that implements mail
delivery is one of the four with no seat.

**Every mounted pin is stale, including the ones with nothing filed.** `station-node`,
`FCPM/fcpublicmedia.org` and `discovery-written/discoverywritten.com` are all at `4635cfc`,
two commits behind — those two commits being exactly the merge that added mail.
`NCCV/cite-fort-collins` is at `0173104`, 24 behind. So this is not a story about neglected
repositories; **nothing anywhere has advanced since the feature landed two days ago.**

## The working order, cheapest first

Proposed, not done. Each step is a pull request against the repository that owns the thing.

1. **Bump the two pin-only repos** — `constellation.anecdote.channel` and `Chaevity/ablative`.
   Five of the 22 items become deliverable for two one-line changes, and both repos are already
   in `rounds.conf`, so the next round proves the loop end to end on real mail.
2. **Bump `data-pile` and `library.anecdote.channel`, and add them to `rounds.conf`.** Four more
   items. The rounds line is a `station-node` change; the pin is each repo's own.
3. **Decide whether `anecdote.channel` gets a seat.** Five items — the largest single block, and
   it is already in `rounds.conf`, so a seat is the only thing missing.
4. **Decide the seat question for `civic-node`, `tell`, and `advocate` itself.** Nine items. These
   are real decisions about who speaks for those repositories, and should not be bundled with
   anything mechanical.

**Steps 3 and 4 are not chores and should not be rushed.** An unseated repository is not a bug; it
is a repository nobody has decided to speak for yet, and `rounds.conf`'s `off` exists precisely so
that stays visible rather than implicit.

## What this does not propose

**Not automatic pin bumping.** The caretaker reporting a stale pin and not advancing it is correct
and should stay correct. This file is the report; the bumps are pull requests.

**Not a response obligation.** A petition is *not owed a response* and `withdrawn` is a real door.
Delivery only means a seat has seen it and said what it did — including declining.

**Not clearing the ground.** Graduation is a person's act at triage. Nothing here changes that.

## Who should hold this

No seat owns this file. The closest existing constituency is `presentation` — *whether this node's
shape still fits what it is doing* — but mail delivery across eight repositories is a cluster
concern, and two petitions already on this ground say so:
`supervise-a-cluster-not-just-a-repository.md` and `the-supervisor-is-an-executable.md`.

**This survey is evidence for both of them.** If either is adopted, this file should become that
seat's, the way [`BOUNDARY.md`](BOUNDARY.md) belongs to `addressing`. Until then it is a draft kept
by whoever last ran the numbers, and the numbers are reproducible from the commands in the survey.
