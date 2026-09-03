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

## Instanced behaviour is not canonical behaviour

The engines are **gloves**: powerless machinery a node puts on so it can act like a Tell, an Atlas,
an Antidote in official ways. **`civic-node` wears them**, and therefore hosts their workflows — so
it is the nexus for what the engines *do*, and the credential for an engine's role lives where the
INSTANCE is, not in the engine's own repository.

An engine's **canonical** repository behaves differently and usually needs far less. Canonical
`tell.anecdote.channel` serves a page that matters and is fairly inert; `journal.anecdote.channel`
and `judgement` reference **no credentials at all**. Those are not gaps — they are the engines
being engines.

So `civic-node` holding seven secrets is not sprawl. It is one node instancing several roles, and
each secret is the battery for one of them:

| workflow | role being instanced | battery |
| --- | --- | --- |
| `antidote-heartbeat`, `antidote-intake` | antidote | `ANTIDOTE_LEDGER_KEY` |
| `bill`, `register-peer` | atlas | `ATLAS_SIGNER_KEY`, `ATLAS_PR_TOKEN` |
| `register-self` | tell (registering itself) | `TELL_SIGNER_KEY` |
| `antibody` | publish + cache | the Cloudflare pair |

**Read a missing battery as an unarmed role, not a broken one.** A node may declare a role before
it can perform it — `antidote.yml` and `atlas.yml` sit at this node's root while `AGENTS.md` calls
antidote *skeleton status*. Declaring early is honest; the declaration is a statement of what the
node is, not a claim that every part of it is wired.

## Where that reading stops being generous

**An unarmed role must not be a role that fires anyway.** Invariant #5 says honest defaults fire
nothing, and a scheduled workflow whose battery is absent is the counter-example:

- `antidote-heartbeat.yml` **failed on 2026-09-01** and has **no guard** — it reads
  `ANTIDOTE_LEDGER_KEY`, which exists in neither the repository nor the organisation. A scheduled
  job failing on a cadence nobody watches is indistinguishable from one that is merely not
  provisioned yet, which is how it stayed like that.
- `bill.yml` and `register-peer.yml` read `ATLAS_SIGNER_KEY`, also absent, and have **never run**.
  Unarmed and unexercised — so nothing has told anyone.

The fix is not necessarily to mint the keys. It is that a workflow for an unarmed role should
**decline and say so**, the way `acm-sync` does, rather than fail obscurely or wait to.

## One that is a plain mismatch

`civic-node` reads `secrets.CLOUDFLARE_ZONE_ID` while the value exists as an organisation
**variable** of that name. Secrets and variables are different namespaces; the read resolves empty.
The third instance of that exact shape in this constellation in one day.

## Castling — taking an address from one repository and giving it to another

A move like this is an **addressing event**, not a housekeeping one: a new address is a new
signature, whoever the vendor is. It is documented rather than performed quietly, and what must be
enumerated first is exactly the table above — because the thing that does not survive the move is
never the code.

**Nothing here promises survival.** The point is only that the requirements are known before they
are urgent, so that replacing a shell is a lookup rather than a spontaneous research project.
