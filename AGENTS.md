# constellation.anecdote.channel — orientation

A **node**: anyone running engines. Not a civic node — that is one *kind*, and kinds are names for
configurations, not classes of thing.

| Your question | The one place |
| --- | --- |
| What is this and what is deliberately not wired? | [`README.md`](README.md) |
| Who speaks for this node, and what do they want? | [`advocate.yml`](advocate.yml) |
| How does an advocate session work? | `.advocate-engine/METHOD.md` |
| What do `draft` / `ready` / `promoted` mean? | `.advocate-engine/STATUS.md` |
| How is it run without an API or a bill? | `.advocate-engine/LOCAL.md` |
| What binds the mailbox? | `.tell-engine/CONSTITUTION.md` |

## Working here

- **The engines are mounted, not maintained.** Change an engine in its own repository; only its
  pin moves here.
- **Advocate branches are workspaces, never merged.** `advocate/<name>` carries a seat's
  `POSITION.md`, `COMPLAINTS.md`, `ASKS.md` and `sessions/`. `main` does not learn about them.
- **Both seats are drafts.** They were transcribed from Autumn's framing, not invented, and the
  voices in them are the part most worth rewriting. A constituency cannot be inherited or guessed.
- **`draft` is safe.** Write the half-formed one; nothing is owed for leaving it at `draft`.
