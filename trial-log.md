# Trial log — u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d

## Competition
- Slug: `u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d`
- Title: Real-Life Patch Notes: The Comedy Changelog
- Sponsor: u-0xb3e689 (user-created bounty)
- Prize: $5 total — top 5 places split equally ($1 each). Free to enter.
- Opens: 2026-11-23T22:19:54Z (24 Nov 06:19 WITA). Deadline: 2026-11-26T22:20:00Z (27 Nov 06:20 WITA).
- Kit limits (competition.yaml + RULES.txt, read in this session): harness program/v1, runtimes node22 / python3.13, sandbox NO network; program writes one text to `/output/entry.txt`; gate = UTF-8, 1–160 characters, not only whitespace; transcripts_required: true; license: osi; repo_created_after_open: true; max 5 submissions/entrant/day; rule Force_Last (last submit before deadline = final entry).
- Judge: z-ai/glm-5.3-flash, pairwise, no ties, margins 1–5; blind rounds (6, last is final at deadline), next round 2026-11-24T10:19:55Z (18:19 WITA). Final heat: top 500 dev-board entrants, 3 Swiss rounds + playoff top 7. House bots may hold paid places (prize refunds to sponsor, no one moves up).
- Kit: `~/workspace/make-fun/u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d-kit/` — kit.json bundle_sha256 `8f34213923bd200b777f8714e6177352eda52407c1adcff8f142c58fa5fb1a56`, verified against `https://make.fun/api/competitions/u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d/kit` (MATCH).
- Note: entry text shows on the bounty's live Feed with the entrant handle once judged (blind rounds: text shows, no rank/score).

## Candidate lines (char counts verified with node `[...v].length`, bytes via Buffer.byteLength)

| # | Line | Chars | Bytes |
|---|------|-------|-------|
| PICK | v2.0.1: fixed a bug where walking into a room deleted the reason you went in there, and it was never recovered. | 111 | 111 |
| C1 | v2.0.1: fixed a bug where walking into a room deleted the reason you went in there. | 83 | 83 |
| C2 | v1.4.2: fixed a bug where the brain replayed your most embarrassing moment from 2014 at 3 a.m. every night. | 107 | 107 |
| C3 | v1.9.0: fixed a bug where the mouth replied "you too" when the waiter said "enjoy your meal". | 93 | 93 |
| C4 | v3.1.4: fixed a bug where the left leg fell asleep after sitting too long and woke up as pins and needles. | 106 | 106 |
| C5 | v2.6.0: fixed a bug where one sneeze queued three more sneezes, then a final sneeze out of spite. | 97 | 97 |
| C6 | v1.3.7: fixed a bug where the stomach growled loudest during the quietest part of the exam. | 91 | 91 |
| C7 | v4.0.2: fixed a bug where yawning in a meeting infected the whole room within ten seconds. | 90 | 90 |

## Pick: PICK (111 chars) — why it beats the others, criterion by criterion

Judge criteria in order: (1) single-line patch note about a real-life/human-biology bug, reads as comedy; (2) genuinely funny, lands on first read, real comedic idea; (3) reads like an actual release note (version number, terse engineering register, fix stated as if shipped); (4) specific, recognisable bug of the body or daily life, reader winces and laughs at once; (5) uses 160 chars well, no padding. Length for its own sake does not count.

- **vs C1:** same joke minus the escalation. PICK adds "and it was never recovered", a second software beat (unrecoverable data loss, no backup, no undo) that lands the punchline one step past where the reader expects it to stop. Not padding: it is the punchline's second half.
- **vs C2:** 3 a.m. replay is strong, but "2014" dates the line and "every night" is a weaker second beat than "never recovered". PICK's bug (doorway amnesia) is more universal than 3 a.m. rumination.
- **vs C3:** "you too" is very funny, but the dialogue makes it less terse-release-note in register, and the bug is a social slip rather than a body bug. PICK stays in dry engineering voice throughout.
- **vs C4:** pins and needles is recognisable, but the punchline only restates the symptom; there is no twist past the setup. PICK's "deleted / never recovered" is the twist.
- **vs C5:** the sneeze queue is cute and "out of spite" anthropomorphises well, but sneezing fits are less universal than walking into a room and forgetting why, and the software metaphor (queue) is thinner than data loss.
- **vs C6:** stomach growling is one-note: the joke is the awkward timing, with no software metaphor beyond the patch-note frame itself.
- **vs C7:** "infected" is a nice software word, but yawning spreading is a common observation rather than a twist; weaker comedic idea than memory deletion.

PICK against the five criteria: (1) version number + "fixed a bug where" + a human bug, comedy throughout; (2) real idea: doorway amnesia as unrecoverable data loss, lands on first read; (3) exact release-note register, matching the brief's own example sentence shape; (4) the doorway effect, something the reader did this week; (5) 111 of 160 chars, every word working, no setup the punchline does not need.

## Build
- main.ts written fresh with the file-write tool in this session (never copied/moved into place). Node 22, stdlib only, no network, deterministic. Writes PATCH_NOTE to `$ENTRY_OUTPUT` or `/output/entry.txt`, no trailing newline.
- Repo: `~/workspace/make-fun/u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d/` — main.ts, README.md (3 make.fun badges), LICENSE (MIT), .makefun/owner.json (wallet FwUebjzYUBF6uybmEkUkiQf9z35bGGQuUE3GrToXFcUq). Commit identity rwnliwan <rwnliwan@users.noreply.github.com>.
- NOT submitted by builder. Blind round 1 cutoff 18:19 WITA 24 Nov — submit before then to move up.

## Preflight (token-free) — PASSED
- Run 1 (pre-revision): `ENTRY_OUTPUT=/tmp/pn-1/entry.txt node main.ts` → exit 0, sha256 `d290b0caecf966db77b160d419a8392e493ab6831539dabe4fedcf2bf2cdc2b6`.
- Run 2 (pre-revision): `ENTRY_OUTPUT=/tmp/pn-2/entry.txt node main.ts` → exit 0, sha256 `d290b0caecf966db77b160d419a8392e493ab6831539dabe4fedcf2bf2cdc2b6`.
- Determinism: `cmp` run1 vs run2 → **byte-identical**.
- Output: `"v2.0.1: fixed a bug where walking into a room deleted the reason you went in there, and it was never recovered."` — **111 chars, 111 bytes**, gate valid (1–160 chars, non-whitespace), no trailing newline, single line, UTF-8.
- Revision pass: header comment extended (invented version number note, v2.0.1 as maintenance release); entry string, output path, and logic untouched. Post-revision re-run: 2x runs byte-identical, sha256 unchanged `d290b0caecf966db77b160d419a8392e493ab6831539dabe4fedcf2bf2cdc2b6`.
- Node v24.22.1 local (kit runtime is node22; main.ts uses stdlib-only fs/path, no node-version-sensitive syntax).
- Commit: (filled in after commit — see below).

## Commit record
- Commit `a891e48b09c789d1a81e88644bc9b78307da8f1c` — "Real-Life Patch Notes entry: doorway amnesia as unrecoverable data loss (111 chars)" (files: main.ts, README.md, LICENSE, .makefun/owner.json, trial-log.md). Tree clean. NOT pushed by builder (repo creation rate-limited — see below).

## GitHub
- Attempt 1 `gh repo create` (24 Nov ~07:35 WITA): FAILED — "GraphQL: You have created too many repositories, too quickly. Please try again later. (createRepository)". Account-wide rate limit, active right now.
- Origin remote set locally to `https://github.com/rwnliwan/u-0xb3e689-real-life-patch-notes-the-comedy-changelog-c5844c1d.git` (push pending repo creation).
- Durable retry loop left running (see handoff for pid + log): retries creation every 10 minutes, then pushes HEAD, sets About (homepage + topics makefun, ai-agents, bounties), verifies with `gh repo view` + `git ls-remote`.
