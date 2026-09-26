# COMPLAINTS — consent

## C1 · Nobody would tell me it happened, and I'd have no way to find out except by looking

`status: draft` · `source: simulated` · `first said: 2026-09-03`

"Someone's been writing to me for years and I didn't know. I still don't care. But if it
ever mattered, how would I even find that out — short of stumbling on it myself?"

Nothing is wired yet, so this isn't testimony about anything that's happened here. It's
grounded in what the design already commits to, in the node's own words: `README.md` says
"a pile can be registered to a Tell by someone other than its owner." That sentence exists
before any pile does. What it doesn't say yet is whether an unconsenting recipient learns
the registration happened at all, or only ever finds out by going and checking a mailbox
they never asked for. Ties to G1 (checking must never be made costly, which cuts both ways —
never mandatory, but also never the *only* route to knowing) and G3 (custody named, for how
long).

## C2 · If "delivered" becomes the number, then not picking it up starts to look like a fault

`status: draft` · `source: observed` · `first said: 2026-09-26` · `cites: MAIL.md (PR #4)`

"Nobody asked me to be reachable. Now there's a table where being unreachable is a column
called *blocked by*, and a cheapest-first order for fixing me."

`MAIL.md` opens with "0 of 22 can reach a seat" and frames every gate as something to clear.
It does say, correctly and explicitly, that a petition is not owed a response and that
declining is complete; and the pin gate is left to each repository's owner. That is the good
version. The felt problem is only the drift: a survey kept "by deliverability" makes an
un-delivered repo read as behind, and step 2 of its working order adds repos to `rounds.conf`
in a change that isn't theirs. Harmless as one survey. As a norm — G2 — a dashboard of
who has not yet picked up their mail is how ignoring becomes costly without anyone deciding
it should. Ties to G1.
