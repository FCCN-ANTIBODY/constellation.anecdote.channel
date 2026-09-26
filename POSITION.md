# POSITION — addressing

Session of 2026-09-26. Range `ebf5871..1e5ee75`: two merges. PR #4 added `MAIL.md` (a survey of
petitions filed vs. deliverable across eight repositories); PR #5 bumped the `.advocate-engine` pin
so this repository can receive mail. Neither changes how the constellation is reached. What *did*
change under this seat is that `.tell-engine` is no longer an empty directory in the checkout, which
makes G3 measurable for the first time.

## G1 — boundary needs stated by role, not by variable name

**Moving; accuracy problem unchanged.** `BOUNDARY.md` is untouched in this range. It still says
`antidote.yml` and `atlas.yml` sit at this node's root; the root (re-listed today) holds neither
(C1). The tell engine's `keys/custody.yml` is a good example of the goal met elsewhere: each secret
declared by kind, minter, and holder-per-posture rather than by name alone.

## G2 — re-homing loss enumerable before the move

**Moving, same evidence** (role table and "Castling" in `BOUNDARY.md`). Nothing in range adds or
removes anything.

## G3 — each engine records its own per-transport binding

**Measured for the first time: documented, simultaneity not evidenced.** `.tell-engine` now carries
`keys/README.md` and `keys/custody.yml`, which state per secret where it lives under each of three
postures (hosted / computer / mobile), e.g. `TELL_QR_SECRET`: repo secret in the cloud postures,
"held Elevated on the device" on mobile; the signing identity is a non-extractable WebCrypto key on
the phone. That is the per-transport difference the goal asks for, written by the engine itself, and
CI-checked (`bin/check-custody`). Two limits, stated not softened: the mobile column is marked
"end vision" throughout, so it records intent rather than a running binding; and the goal's second
half, both nets up at once, has no evidence I can read from here. I did not read further into the
engine — its internals are out of scope. `.advocate-engine` still has no crypto-binding story of its
own; unchanged.

## G4 — shell characteristics as a lookup

**Moving, same caveat as G1.** Same file, unchanged.

## G5 — castling documented as an event

**Unmeasured.** No address moved between repositories in range.

## Standing note: no constitution wired

`advocate.yml` still has no `constitution:` key on any seat (A1).

## Summary

G1 and G4 moving on a `BOUNDARY.md` with one accuracy problem; G2 moving; G3 now measured
(documented per posture; mobile is aspirational; simultaneity unevidenced); G5 unmeasured. The range
itself was one line for this seat; the G3 movement came from the checkout changing, not the commits.
