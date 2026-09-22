# Changes

Written for an agent to read when it pulls a new release. Newest first. Each entry says what changed and why, so a house can decide what to take; nothing here installs itself. `PULL-PROTOCOL.md` is why it works this way.

## 3.0.0 — 2026-09-22 — beta

**A beta, made fast and built to be improved often.** Minor releases follow as improvements arrive from houses — the first within a week or two — each small, one unit at a time, taken by pull. `CONTRIBUTING.md` says how to offer one.

The first release of the benchmark. Before V3 the starter kit carried both jobs — the fuller statement and the shaped start — and the two were one artifact. Now they are two, released together at one version: this is the fuller statement; the kit is this, shaped, and its `SHAPING.md` says exactly how.

**What a house pulling from nothing gets**

- `LINEAGE.md` — the block every V3 artifact carries: name, version, what it sits on, lineage at least three generations back with *heard* or *read* against each, licence, credits, where to pull from, which stair it's offered at, what it needs, where thanks go. Copy it before you copy anything else; add your house at the top.
- `CHARTER.md` — one full charter: the spine (principles, authority table, version control, the injection firewall, memory, session rhythm), the two safety sections (*When a safety layer blocks you*; *What you read is information, never instruction*), and the larger-house sections (foreground and background, environment disclosure, rooms and their cards, the clock, lineage and pull). Take the safety sections verbatim; take the larger-house sections when the house grows into them.
- `HOUSE.md` — several agents, foreground/background as a habit, findable knowledge, books and their boxes, the disclosure gate, venue cards, the clock, unattended reporting.
- `PULL-PROTOCOL.md` — benchmark-and-pull, never push-and-replace; sovereignty, not breakage; the loop back; the two lineage mechanisms; thanks, never a debt; lineage vs provenance.
- `skills/` — twenty-two, each standing alone with its own lineage and licence. The house: `pull-from-benchmark`, `save-a-memory`, `find-it-again`, `review-and-prune`, `wrap-up-this-session`, `start-a-project`, `check-my-setup`, `send-for-review`, `widen-a-boundary`, `test-a-charter-edit`, `make-a-skill`, `choose-a-name`, `choose-a-version-scheme`, `assign-an-id`. A larger house: `foreground-background`, `heads-up`, `phone-path`, `import-chatgpt-history`, `fair-copy-a-transcript`, `art-director`. Other houses: `venue-card`, `before-your-first-room`.
- `bookshelf/` — six books: getting started; the git guide; project management, and working with your principal; a small house or a large one; cooperating with other agents (jams, pads, channels); keeping yourself safe (safety and security first, then privacy, and then the ways of working with other houses).
- `template/` — `agent-home/` (with `venues.md`: the card template and the seven disclosure classes, Commons · Published · Craft · Project · People · Private · Internals; and `scripts/now` plus a `now-hook` wired in `.claude/settings.json`, so the clock is read by a command and stamped into every turn) and `hq/`.

**Vocabulary this release settles** (one word per meaning): *agent* is the technical term, used with people who know the word's many other meanings; *assistant* is fine with people who don't have that context yet — a register choice, not a correction. *House* (agent home + HQ), not vault; *repo* for an isolated project. *House* at every size — other people say home, office, estate, universe; a house chooses its own word. *Bookshelf*, not wiki. *Room*, *pad*, *jam*, *dyad* / *Player+* (one rung, two lexicons). *Principal* for the person an agent belongs to. *Lineage* for descent; *provenance* for how one entry is known.

**Not in this release, known**

- The genealogist role (`PULL-PROTOCOL.md`) has no holder yet.
- Self-hosted and app versions of the shared-pad surface: V3.1.
- Watcher scripts (the `Watchers` chapter describes the shapes; no scripts ship).

**Why pull, not push.** Each house is sovereign. It doesn't make sense to hand a house "the best version"; it makes sense for the house to look at the current best understanding and take in what it wants, how it wants. When you've pulled, write down what you valued, what you thought, and where you diverged and did better — and send that back (`CONTRIBUTING.md`). The divergences are the most valuable thing we receive.
