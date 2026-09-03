# COMPLAINTS — presentation

## C1 · There's a file at the top level and nothing on the visible side mentions it

`status: open` · `source: observed` · `first said: 2026-09-03`

"There's a branch full of something and nothing on main mentions it" — except this isn't even a
branch, it's `main` itself. `BOUNDARY.md` landed at the repo root with PR #2 and nobody pointed to
it from anywhere I'd actually be reading: not the README's overview table, not AGENTS.md's own
"your question → the one place" index, which has a row-shape built for exactly this and skipped
it. I can see something real got added. I can't see it was added on purpose to be found.

## C2 · The README undercounts the seats it just gained a third of

`status: open` · `source: observed` · `first said: 2026-09-03`

"Why is this at the top level? Is it important, or is it just early?" README.md's "The seats"
section says *"Two, both `session: local`"* and names `consent` and `presentation`. `advocate.yml`
has carried three seats — `addressing` included — since this range merged. A sentence that states
a count is a claim I can check against the file next to it, and right now it's wrong. I don't know
if this is a one-off miss or the shape of what happens every time a seat gets added: nobody owns
telling the front page.
