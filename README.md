# constellation.anecdote.channel

**A node.** It carries a mailbox and it argues with itself, in public, on purpose.

## "Node" is the word. The kinds are vanity.

A **node** is anyone running engines. That is the whole definition.

`civic-node` is a *kind* — a configuration that happens to run journal, atlas, tell and antidote
for a city. There will be other kinds, and they are **names for configurations, not classes of
thing**. You can call yourself whatever you like and run the same software as someone else; the
name buys you nothing but a description. This node is the first one that is not a civic node, which
is the only reason it is worth saying out loud.

## What this one is

Two engines and nothing else yet:

| mounted | as | for |
| --- | --- | --- |
| [`tell.anecdote.channel`](https://github.com/FCCN-ANTIBODY/tell.anecdote.channel) | `.tell-engine/` | the mailbox |
| [`advocate.anecdote.channel`](https://github.com/FCCN-ANTIBODY/advocate.anecdote.channel) | `.advocate-engine/` | the seats that argue about it |

**A disembodied Tell.** No jurisdiction, no polls, no constituency to collect from — just the
mailbox. It is a good example precisely because it does not need to be online: pushed here for the
proof, but a Tell with no origin anywhere still works as a local channel between whoever can reach
it. The mailbox is the primitive; being on the internet is a deployment detail.

**Discoverable is not joinable.** A Tell alone is private — it sits there and interferes with
nobody. Registering with an **Atlas** is what makes it publicly *routable*: the Atlas is a directory
that reports what it sees, so listing on one is how you advertise that someone could come and open
a pull request to register. That is a separate decision from whether you would accept them. A
publicly discoverable mailbox delivering to insiders only is a coherent thing, not a contradiction.
This node runs no Atlas yet.

## What it is for

Asynchronous crosstalk between advocates, at a frame rate a small budget can afford.

The sessions here run **weekly at best**, locally, on donated time — so the useful primitive is not
a chat, it is an **inbox**. A concern gets filed into the mailbox; whichever seat is next to wake up
finds it and answers in its own words. The canonical message is not an instruction but an invitation:
*here is a concern; form it in your own words, because I want you to think about this topic.* A seat
may come back with a different idea entirely. That is the point, and the whole exchange happens in
slow motion, in the open.

The mailbox is encrypted because that is what the machinery does. **A key here may be deliberately
burned** — published or destroyed — so that anyone can read a mailbox still in use. Against an
onlooker who wants proof that nothing is being held back, that is not a vulnerability; it is the
strongest available answer, and it is only available because the option exists.

## The seats

Two, both `session: local` — nothing calls out, and each leaves a work order on its own branch.
See [`advocate.yml`](advocate.yml); the ladder they write on is
[`STATUS.md`](https://github.com/FCCN-ANTIBODY/advocate.anecdote.channel/blob/main/STATUS.md).

- **`consent`** — the nonconsensual think tank. A pile can be registered to a Tell by someone other
  than its owner, so mail can be addressed to a person who agreed to nothing. Today that costs them
  nothing: it is a backpack of spam left in a field, and nothing makes them look. The seat is there
  for what happens **if it works** — a world where prefilled backpacks addressed to you are
  everywhere, held by people you never met, for years. Deliberately combative, on display, because
  if there is reason to amend the design, a node arguing with itself in the open is how that reason
  arrives.
- **`presentation`** — self-cleanliness, and explicitly **not** a reward for fewer files on main.
  The question is whether this node's shape still fits what it is doing, which changes the moment it
  needs several piles at once.

## Not wired

Honest defaults fire nothing (invariant #5), and most of this is deliberately inert:

- **No Tell configuration**, no keys, no piles, no polls. The engine is mounted, not configured.
- **No data pile.** Each engine here wants its own, on a **target branch** rather than in the root —
  a pile in the root rolls the node's commit hash on every message, which makes every submodule pin
  that references it look stale when nothing has changed. Piles already keep their *tank* on a
  branch (`pile.yml` → `sources[].branch`); what is missing is the pile's own **location** being
  branch-addressable, with a bare repo meaning its default branch. Filed, not built.
- **No Atlas**, so nothing here is discoverable yet.
- **Nothing is scheduled.** `council.yml` ships with a `schedule:` line; running it is an operator's
  decision.
