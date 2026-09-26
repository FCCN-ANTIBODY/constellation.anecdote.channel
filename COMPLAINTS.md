# COMPLAINTS — addressing

Session of 2026-09-26. C1 and C2 carried forward unchanged (`BOUNDARY.md` untouched in
`ebf5871..1e5ee75`; re-checked the root listing). C3 closed.

## C1 · The lookup pointed me at two files that aren't there

`status: draft` · `source: observed` · `first said: 2026-09-03` · `re-checked: 2026-09-26, unchanged`

"Which of these do I actually need, and what happens if I don't have it?" `BOUNDARY.md` told me
`antidote.yml` and `atlas.yml` sit at this node's root. I looked. They don't. If I'm re-homing this
and I trust the document that's supposed to be the trustworthy one, I go looking for two files that
were never here, or I stop trusting the rest of the table too.

## C2 · Half of my lookup table is about a repository I can't see

`status: draft` · `source: observed` · `first said: 2026-09-03` · `re-checked: 2026-09-26, unchanged`

"I don't know what this variable was for, and it turns out nobody does." `BOUNDARY.md` spends most
of its length on `civic-node`'s secrets, `civic-node`'s failing workflows, `civic-node`'s naming
mismatches — not this repository's. I can't tell from inside `constellation.anecdote.channel`
whether any of that is still true. If I only ever have this repository, I've inherited claims about
a sibling I have no way to check.

## C3 · The mailbox that actually holds the per-transport key story isn't here to read

`status: answered` · `source: observed` · `first said: 2026-09-03` · `closed: 2026-09-26`

Outcome: `.tell-engine` is now populated in the checkout. `keys/README.md` and `keys/custody.yml`
state each secret's holder per posture (hosted / computer / mobile), and `bin/check-custody` guards
them in CI. The question this asked, whether the engine documents its own half, has an answer: yes.
What remains is narrower and is not this complaint: the mobile column reads "end vision" (see
`POSITION.md` G3).
