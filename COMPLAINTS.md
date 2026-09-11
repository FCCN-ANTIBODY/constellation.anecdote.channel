# COMPLAINTS — addressing

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
