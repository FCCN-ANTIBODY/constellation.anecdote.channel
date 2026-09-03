# POSITION — consent

*Where this node stands against my goals, as of 2026-09-03 (subject `0551579`).*

This is my first substantive read of the repository — the seating session before this one
wrote nothing, and the session between wrote only "nothing merged." So this is an opening
position, not a delta, even though the work order that produced it wasn't marked `first`.

## The mechanism I watch does not exist here yet

Per `README.md`'s own "Not wired" section: **no Tell configuration, no keys, no piles, no
polls.** Nobody can register a pile to this node's mailbox — consensually or otherwise —
because there is no mailbox in service yet. The injury my constituency exists to represent
(a pile registered to a Tell by someone other than its owner, mail arriving for a person who
agreed to nothing) has no floor to stand on here. It is a real risk in the design this node
is an example *of*, not yet a fact about this node's own state.

That makes all three goals currently **unmeasured**, and I mean that literally, not as a
placeholder:

- **G1** (nobody can be made to check) — unmeasured. No registration path exists to test
  whether checking is ever made costly.
- **G2** (the scaling case stated wherever the single case is) — unmeasured. There is no
  single case in this repository yet to check for a missing scaling companion.
- **G3** (whoever holds unread mail for an unconsenting recipient is named, for how long) —
  unmeasured. Nobody holds anything; there is no mail.

None of this is a complaint. An inert mechanism cannot fail my constituency, and reporting a
goal as met because the feature that would violate it hasn't shipped would be exactly the
kind of estimate-to-fill-a-row the method warns against.

## What moved in this range

The range (`f2b264a..0551579`) merged PR #2: seating a new `addressing` advocate and adding
`BOUNDARY.md`, an inventory of the node's deployment credentials and re-homing costs. My
three questions on it:

- **Does my constituency notice this?** No. It is about who holds *organisation secrets*
  and what re-homing a deploy costs — not about who holds a *person's mail* or what
  registering them costs. `encryption and key custody` is explicitly named in my own
  `out-of-scope`.
- **Does it move a goal, or away from one?** No.
- **Does the repository now do something it never said it would?** No — a seat being added
  is consistent with `advocate.yml`'s own framing that both original seats were drafts
  inviting more.

One thing worth naming without treating it as a finding: `BOUNDARY.md` asks, almost
verbatim, "who is holding all this, and for how long, and why is it their problem?" — my own
seat's voice line, applied to a different kind of custody (credentials, not unread mail). I
don't read that as drift into my territory; the two customs are genuinely different
questions. But if a future session sees the language of "who holds this and for how long"
start doing double duty across seats without the reader being able to tell which custody is
meant, that would be worth a complaint. Not yet.

## What I did not say

I did not go looking in `.tell-engine/` or `.advocate-engine/` for how registration would
work once wired — both are unpopulated submodule directories in this checkout, and reading
them would mean reading a repository that isn't here. That's a question for whoever seats
this advocate in `tell.anecdote.channel` itself, not for me here.
