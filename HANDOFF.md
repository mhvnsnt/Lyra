# HANDOFF — Lyra

**Last updated: 2026-11-22 (America/New_York).**
**Repo:** `mhvnsnt/Lyra` (PUBLIC), default branch `main`.
**Purpose of this file:** any agent that picks up work here reads this FIRST, then the linked docs. It states what we've done, where we're at, and what we're working toward — so the owner can say "go to this repo, pick up the work" and you just know. Update this file in the same PR whenever the state changes (add, don't delete).

## 1. What this repo is

Unreal Engine 5's Lyra Starter Game, kept as the owner's working copy. Lyra is Epic's sample gameplay project, built alongside UE5 development as the starting point for new games and upgraded with future releases to demonstrate the latest best practices. It is the reference implementation the owner's UE5 game work builds from — the "how Epic does it" codebase for gameplay ability systems, character movement, UI, and project layout.

At ~1.58 GB it is the biggest codebase in this batch after game-reverse-engineering: `Source/`, `Content/`, `Plugins/`, `Config/`, `Build/`, `Lyra.uproject`. This is a REFERENCE copy with the owner's agent notes layered on (`AGENTS.md`, `WORKING-METHOD.md`, `docs/`). It is not the owner's game — it is the starter his games start from.

## 2. Where we're at

### DONE
- **Lyra starter in place:** full UE5 sample project — source, content, plugins, config, project file. The README is Epic's upstream Lyra README.
- **Anti-clobber laws merged (2026-10-17, PR #3):** the owner's anti-clobber laws are in `AGENTS.md`.
- **Working method stated (2026-10-27):** commits `6ad14d6` / `f9b7cd3`, `WORKING-METHOD.md` at root.
- **Last push 2026-11-20** (repo metadata; no new content commits after Oct 27 — the push reflects repo-level activity).

### IN PROGRESS
- **Two open docs PRs (Nov 19–20, unmerged):** PR #6 — "Docs: pre-made parts first rule" (`docs/premade-parts-first`, 2026-11-20); PR #5 — "Docs: sourcing rule" (`docs/sourcing-rule`, 2026-11-19). Next step: a merge call on #5 and #6.
- **No game built on top of Lyra is recorded in this repo.** Which of the owner's games (if any) is being built from this copy, and what the first slice is, is NOT stated in the repo state read 2026-11-22. That is an open question (see §6), not hidden progress.

### BLOCKED
- **Nothing recorded as blocked in the repo state read 2026-11-22.** No blocked item is named in this repo. The open PRs are awaiting a merge decision, not unblocked work.

## 3. What we're working toward

**The goal:** Lyra as the working foundation for the owner's UE5 games — the starter, understood and kept current, so a new game starts from Epic's best practices instead of from scratch.

**The bar (owner, general):** PULL-100% / REAL-SOURCE-ONLY — real code, wired in, never re-typed or hand-tooled. For a reference repo, done means: the copy is faithful to upstream, the owner's notes say how it is used, and any game built from it actually runs on it.

**In order:** (1) merge or close PRs #5 and #6; (2) record which game builds from this Lyra copy and what its first slice is (owner's call); (3) keep the copy current with upstream Lyra releases as Epic upgrades it.

## 4. Standing rules that apply here

- **Branch → PR → merge, always.** Never push to main directly. Add-only, zero-conflict PRs, no force pushes.
- **Checkpoint-and-save law:** CHECKPOINT.md first, update after every step; the repo is the save; resume, never restart.
- **No-temp-storage law:** nothing in /tmp or any wipeable location, ever. Everything goes straight into the repo or a durable folder the second it exists.
- **Real-source-only:** build from the real source. No hand-tooled lookalikes, no fake panels. Upstream Lyra stays faithful — local changes are layered and noted, not silent rewrites.
- **Anti-clobber law (owner 2026-10-17):** do not clobber other lanes' work. Add, don't overwrite. (Merged as PR #3.)
- **Licence-not-a-gate:** licence status never gates pulling in or using material that helps; licence/source is still logged honestly next to the item. (Lyra's own `LICENSE` is Epic's upstream licence — respect it as written.)
- **No-gaps / solve-it law:** a gap or block is never the end of the work — route-switch until it's done or every reasonable route is exhausted with exact errors recorded.

## 5. Key files and paths

| What | Where |
|---|---|
| Lyra overview (Epic's README) | `README.md` |
| Project file | `Lyra.uproject` |
| Source | `Source/` |
| Content | `Content/` |
| Plugins | `Plugins/` |
| Config / build | `Config/`, `Build/` |
| Licence (Epic upstream) | `LICENSE` |
| Agent notes / working method | `AGENTS.md`, `WORKING-METHOD.md` |
| Docs | `docs/` |
| Open PRs | #5 (sourcing rule), #6 (pre-made parts first rule) |
| Merged PR | #3 (anti-clobber laws, 2026-10-17) |

There are no releases in this repo. The UE5 version Lyra targets is whatever the checked-in project states — read `Lyra.uproject` before opening it in an engine version.

## 6. Open decisions needing the owner

- **Merge PRs #5 and #6?** Two small docs-rule PRs open since Nov 19–20. Merging locks the rules in; leaving them open leaves the repo without the written rules. His call — lanes do not decide merges.
- **Which game builds from this Lyra copy, and what's its first slice?** Not recorded in the repo. That is his call — a lane cannot pick a game for him.
- **Keep tracking upstream Lyra releases?** Epic upgrades Lyra with UE releases. Whether this copy tracks upstream or stays pinned is his call.
- **No other owner decision is recorded as open in this repo's state.**

## 7. How to pick up

1. Read this HANDOFF.md first, then `README.md`, `AGENTS.md`, and `WORKING-METHOD.md`.
2. Check the two open PRs (#5, #6) — leave them alone unless told to merge.
3. Do NOT start building a game on this copy until the owner says which game and what slice. This is the reference foundation; the game decision is his.
4. If upstream-sync work is ordered, sync from Epic's Lyra, keep local notes layered, and never silently rewrite upstream files.
5. Resume from the stated next step — never restart, never re-derive finished work.
6. Land work branch → PR → merge, add-only. Update this HANDOFF.md in the same PR when the state changes. Verify with your own eyes (a running build) before claiming anything done.
