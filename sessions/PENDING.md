# Work order — consent

**A session is due and no machine ran it.** Everything mechanical is already done: the branch is
prepared, the pin is recorded, and the range below is what moved. What is missing is the part that
needs judgement.

- **Advocate:** `consent`  ·  **Branch:** `advocate/consent`
- **Subject commit:** `1e5ee750153c4721fb705f04e52f6a4d32aa55ef`
- **Range:** `ebf58718a64e823ce76c6e1e804685c78198091e..1e5ee750153c4721fb705f04e52f6a4d32aa55ef`
- **Mail:** _no petition space — nothing addressed here_
- **Opened:** 2026-09-14

## What moved

| commit | date | subject |
| --- | --- | --- |
| `1e5ee75` | 2026-09-11 | Merge pull request #5 from FCCN-ANTIBODY/bump-engine-for-mail |
| `12d664f` | 2026-09-11 | Merge pull request #4 from FCCN-ANTIBODY/mail-that-cannot-be-delivered |

## Doing it

1. Read the method: [`.advocate-engine/METHOD.md`](.advocate-engine/METHOD.md). It is law; follow it in order.
2. Your seat — mission, constituency, voice, goals, out-of-scope — is in `advocate.yml` under
   `consent`. Read it. It is the only thing that says what to want.
3. **You are already standing in your workspace.** `POSITION.md`, `COMPLAINTS.md` and
   `ASKS.md` are here, carried forward from last time. Rewrite `POSITION.md` whole; carry the
   other two forward with your edits.
4. Write `sessions/2026-09-14.md` — the range, what changed, what
   you did with each unread petition, and what you deliberately did **not** say.
5. **Delete this file.** An order left behind reads as a session still owed.
6. Commit on this branch and push. Never merge it into `main`.

<!-- machine-readable; bin/pending.mjs reads the block below -->
```json
{
  "advocate": "consent",
  "branch": "advocate/consent",
  "subject": "1e5ee750153c4721fb705f04e52f6a4d32aa55ef",
  "since": "ebf58718a64e823ce76c6e1e804685c78198091e",
  "range": "ebf58718a64e823ce76c6e1e804685c78198091e..1e5ee750153c4721fb705f04e52f6a4d32aa55ef",
  "first": false,
  "quiet": false,
  "commits": [
    {
      "sha": "1e5ee750153c4721fb705f04e52f6a4d32aa55ef",
      "date": "2026-09-11",
      "subject": "Merge pull request #5 from FCCN-ANTIBODY/bump-engine-for-mail"
    },
    {
      "sha": "12d664fd05b8410f2e2435cf789b1aeb7fdbfae0",
      "date": "2026-09-11",
      "subject": "Merge pull request #4 from FCCN-ANTIBODY/mail-that-cannot-be-delivered"
    }
  ],
  "writes": [],
  "constitution": null,
  "petitions": {
    "address": null,
    "filed": 0,
    "unread": 0
  }
}
```
