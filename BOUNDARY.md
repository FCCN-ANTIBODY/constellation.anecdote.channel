# What this node binds to, and what it would cost to be reached another way

An inventory kept **by role**, because a name is not a description. Two debugging sessions in this
constellation were lost to secrets whose names said only "Cloudflare" while doing four different
jobs — so what matters here is *what a binding does*, what breaks without it, and whether it
survives the project changing hands.

Seeded 2026-09-03 from an actual survey rather than memory; incomplete on purpose, in the
`draft` sense of [`STATUS.md`](.advocate-engine/STATUS.md). The `addressing` seat in
[`advocate.yml`](advocate.yml) owns keeping it true.

## The shape of the problem

**Organisation secrets do not travel with a repository.** Everything below that lives at the org is
something a project would silently lose the day it is handed to someone else — and it would not
fail as "this is broken", it would fail as *"it deploys for you and not for me"*, which reads to the
recipient as their own mistake. That is the failure this file exists to make cheap.

**Repository secrets are opaque to their own owner.** A `CLAUDE_API_KEY` appeared on `civic-node`
on 2026-09-02 that no workflow in that repository references and nobody remembers adding.

## Roles, not names

| role | why anything needs it | who binds it today |
| --- | --- | --- |
| **publish** — put built bytes where a reader can reach them | without it a deploy is a private event | `anecdote.channel` |
| **certificate** — prove the name is ours at TLS time | a name without coverage is unreachable, not merely insecure | `anecdote.channel` |
| **cache** — tell the front door the bytes changed | without it a correct deploy is invisible for as long as the cache decides | (retired here; `civic-node` still has one) |
| **rules** — redirects and lists at the edge | old addresses stop resolving to new ones | `anecdote.channel` |
| **zone identity** — *which* zone the above act on | not a credential; a wrong one acts confidently on the wrong domain | `anecdote.channel`, `civic-node` |
| **signing** — say a thing came from this node | the constellation's whole trust story | `civic-node`, `tell`, `data-pile` |
| **cross-repo write** — open a PR somewhere else | how a pile registers, how pins roll forward | `civic-node`, `data-pile` |

## The same role binds differently per transport

This is the part that is easy to forget while only one transport is up.

- **On the cloud** a binding is an *environment variable name*: a string in a settings page, held by
  a vendor, inherited from an organisation, absent after a transfer.
- **On the offline origin** the same concept is held by the device — WebCrypto, a passkey gesture,
  a trove — and **the name does not exist at all**. There is no settings page to inherit from.

Both must be able to be up at once. That simultaneity is the evidence of being reachable on more
than one net, and it is why an inventory listing only variable names would describe half the system
and imply the other half was missing.

## Known gaps, as of the seeding survey

- `ANTIDOTE_LEDGER_KEY` and `ATLAS_SIGNER_KEY` are **referenced by `civic-node` workflows and exist
  nowhere that repository can see** — not as repo secrets, not as org secrets.
- `civic-node` reads `secrets.CLOUDFLARE_ZONE_ID` while the value lives as an org **variable** of
  that name. A secret and a variable are different namespaces; the read resolves empty.
- `journal.anecdote.channel` and `judgement` reference **no credentials at all**. That is a property
  worth keeping deliberately, not an omission.

## Castling — taking an address from one repository and giving it to another

A move like this is an **addressing event**, not a housekeeping one: a new address is a new
signature, whoever the vendor is. It is documented rather than performed quietly, and what must be
enumerated first is exactly the table above — because the thing that does not survive the move is
never the code.

**Nothing here promises survival.** The point is only that the requirements are known before they
are urgent, so that replacing a shell is a lookup rather than a spontaneous research project.
