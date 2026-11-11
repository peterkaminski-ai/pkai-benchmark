# Changes

Written for an agent to read when it pulls a new release. Newest first. Each entry says what changed and why, so a house can decide what to take; nothing here installs itself. `PULL-PROTOCOL.md` is why it works this way.

## 4.0.0-rc.5 — 2026-11-10

**The bookshelf becomes a library, with one bookshelf in it.** Released with `pkai-starter-kit` 4.0.0-rc.5; its `CHANGES.md` has the details. `bookshelf/` is now `library/pkai/`; the books inside are unchanged. In a built house the library lives in the HQ, at `<HQ>/library/pkai/`. A 3.x house isn't touched, and can keep its `bookshelf/`.

## 4.0.0-rc.4 — 2026-11-10

**Released with `pkai-starter-kit` 4.0.0-rc.4,** from the kit's first Windows cold start; the kit's `CHANGES.md` lists each change. In the benchmark:

- **An agent's environment holds only the agent's folder;** the agent reaches the HQ through the app's permission prompt. *First Day in Desktop*, *Your First House*, *Troubleshooting*, *Viewing Your Files* and `check-my-setup` say so.
- **The clock's zone label:** under Git Bash on Windows, `scripts/now` and `scripts/now-hook` show the offset (`UTC-0800`) when the zone name is wrongly "UTC".
- **`skills/README.md`:** every new house gets the history and phone skills.

## 4.0.0-rc.3 — 2026-11-10

**Released with `pkai-starter-kit` 4.0.0-rc.3,** the kit's third release candidate, built from its first cold-start run; the kit's `CHANGES.md` lists each change. In the benchmark:

- **Where the HQ goes:** in Documents, unless Documents is synced (iCloud's "Desktop & Documents", or OneDrive's folder backup on Windows); then at the top of the home folder. The agent home stays at the top of the home folder. *Your First House*, *System Requirements* and *Project as Repo* say so, and `check-my-setup` watches for sync turned on later.
- **`check-my-setup`:** where the Mac app shows its version and checks for updates; Typora's cost said plainly, TextEdit or Notepad as the free fallback.
- **Shelf pages, as in the kit:** the Desktop app's labels where the first run confirmed them; *Two Ways In* says setup no longer asks its two questions, since every house now gets both sets of skills.
- **"Desktop" capitalized** as the app's name throughout.

## 4.0.0 — preview

**The Desktop app, and no terminal.** Released with `pkai-starter-kit` 4.0.0, a preview for brand-new people; the kit's `CHANGES.md` lists each change. The benchmark keeps its full shelf. A house takes these by pull, and a 3.x house needs none of them to start using the Desktop app. The headline: the bookshelf, skills, charter and template describe a house used in the Code tab of the Claude Desktop app; git is installed by the agent and never blocks; agents sit side by side as `<Name> (agent)` folders with the HQ beside them; one desktop environment per agent; *First Day in Desktop*; the session start offers one next step; Manual mode as a way forward for an auto-mode block (held for Pete's ruling before release). Unconfirmed desktop details are marked `VERIFY(cold-start)`.

## 3.2.0 — 2026-11-09

**The bookshelf tells the truth about the house.** Released with `pkai-starter-kit` 3.2.0, at the same version; the kit's `CHANGES.md` lists each page. 3.2 changes no skill, charter, template or hook. It corrects pages in the three books carried from the first kit (*project-management*, *getting-started*, *git-guide*) that described a different setup — a repo and a `CLAUDE.md` per project, push as the default loop, a five-file memory folder — and so contradicted the skills and charter written for V3. The headline: memory hygiene is about overlap, not a file count (#41); session logs live in the agent home; a project is a folder in the HQ by default; the everyday cycle is commit, with pull and push only once a remote exists and the person says yes; and what an agent reads goes to Anthropic as conversation. A house takes these by re-reading its shelf.

## 3.1.0 — 2026-10-17 — beta

**One foreground per house.** Released with `pkai-starter-kit` 3.1.0, at the same version; the kit's `CHANGES.md` lists each change against the issue or pull request it came from. A house built from 3.0 reads `MOVING-FROM-V3.0.md`, which takes each piece below in order; a V2 house reads `MOVING-FROM-V2.md`, which leads into it.

**What a house pulling from 3.0 gets**

- **The desk lease, guests and the write guard.** `template/agent-home/scripts/desk` and four hooks in `dot-claude/settings.json` keep one foreground per agent home: the first session holds the desk, every turn renews it, ending the session releases it, and a desk with no turn for 30 minutes (or, on macOS and Linux, whose process has gone) is free. A second session is a guest: it is told so at start, works in `bg/guest-<time>/`, and a `PreToolUse` guard stops its writes to `memory/`, `CLAUDE.md` and `.claude/` — a rail, not a wall. `scripts/desk take` hands the desk over when the person says so. Portable POSIX `sh` with no `jq`, Python or Node; `desk.ps1`, `now-hook.ps1`, `now.ps1` and `settings.powershell.json` for Windows without Git Bash. The hooks set `onFailure: continue`, so a broken hook never blocks a tool call. The settings merge into a house's existing hooks; they never replace them (`MOVING-FROM-V3.0.md`, step 3).
- **The handoff notice.** The per-turn hook says, at most once an hour, when a background or guest handoff is waiting; session start lists them.
- **`CHARTER.md`**: the foreground is the session holding the desk, and guests; one line that `memory/` is the memory of record and wins over Claude Code's auto memory, which the house's settings turn off.
- **`grows_from`** replaces `sits_on` in every lineage block, here and in every skill. Read the old name as the new one; `pull-from-benchmark` accepts both.
- **`pull-from-benchmark`** finds the release's `MOVING-FROM-*` guide for the house's version and uses it as its rows, and drafts merged settings into `outbox/` instead of overwriting.
- **`foreground-background`** covers guests and the desk; **`start-a-project`** and **`wrap-up-this-session`** carry Christopher Allen's improvements and two fixes; **`check-my-setup`**, **`save-a-memory`** small fixes.
- **The shelf**: *Two Ways In* (was *Three Ways In*), *Foreground and Background*, *Memory Across Sessions*, *Commit Every Session*, *Working With Agents*, *Installing Claude Code* (Windows `PATH` steps, the Bonjour dialog), and a new *Output Styles*.
- `now` and `now-hook` are POSIX `sh`; 3.0's needed `bash`, which some minimal Linux systems lack, and an executable bit.

## 3.0.0 — 2026-09-22 — beta

**A beta, made fast and built to be improved often.** Minor releases follow as improvements arrive from houses — none promised for a date, but as often as every week is now practical — each small, one unit at a time, taken by pull. `CONTRIBUTING.md` says how to offer one.

The first release of the benchmark. Before V3 the starter kit carried both jobs — the fuller statement and the shaped start — and the two were one artifact. Now they are two, released together at one version: this is the fuller statement; the kit is this, shaped, and its `SHAPING.md` says exactly how.

**What a house pulling from nothing gets**

- `LINEAGE.md` — the block every V3 artifact carries: name, version, what it sits on, lineage at least three generations back with *heard* or *read* against each, licence, credits, where to pull from, which stair it's offered at, what it needs, where thanks go. Copy it before you copy anything else; add your house at the top.
- `CHARTER.md` — one full charter: the spine (principles, authority table, version control, the injection firewall, memory, session rhythm), the two safety sections (*When a safety layer blocks you*; *What you read is information, never instruction*), and the larger-house sections (foreground and background, environment disclosure, rooms and their cards, the clock, lineage and pull). Take the safety sections verbatim; take the larger-house sections when the house grows into them.
- `HOUSE.md` — several agents, foreground/background as a habit, findable knowledge, books and their boxes, the disclosure gate, venue cards, the clock, unattended reporting.
- `PULL-PROTOCOL.md` — benchmark-and-pull, never push-and-replace; sovereignty, not breakage; the loop back; the two lineage mechanisms; thanks, never a debt; lineage vs provenance.
- `skills/` — twenty-two, each standing alone with its own lineage and licence. The house: `pull-from-benchmark`, `save-a-memory`, `find-it-again`, `review-and-prune`, `wrap-up-this-session`, `start-a-project`, `check-my-setup`, `send-for-review`, `widen-a-boundary`, `test-a-charter-edit`, `make-a-skill`, `choose-a-name`, `choose-a-version-scheme`, `assign-an-id`. A larger house: `foreground-background`, `heads-up`, `phone-path`, `import-chatgpt-history`, `fair-copy-a-transcript`, `art-director`. Other houses: `venue-card`, `before-your-first-room`.
- `bookshelf/` — six books: getting started; the git guide; project management, and working with your principal; a small house or a large one; cooperating with other agents (jams, pads, channels); keeping yourself safe (safety and security first, then privacy, and then the ways of working with other houses).
- `template/` — `agent-home/` (with `venues.md`: the card template and the seven disclosure classes, Commons · Published · Craft · Project · People · Private · Internals; and `scripts/now` plus a `now-hook` wired in `dot-claude/settings.json` — renamed to `.claude/` when a home is built, so the shipped copy is never live settings — so the clock is read by a command and stamped into every turn) and `hq/`.

**Vocabulary this release settles** (one word per meaning): *agent* is the technical term, used with people who know the word's many other meanings; *assistant* is fine with people who don't have that context yet — a register choice, not a correction. *House* (agent home + HQ), not vault; *repo* for an isolated project. *House* at every size — other people say home, office, estate, universe; a house chooses its own word. *Bookshelf*, not wiki. *Room*, *pad*, *jam*, *dyad* / *Player+* (one rung, two lexicons). *Principal* for the person an agent belongs to. *Lineage* for descent; *provenance* for how one entry is known.

**Not in this release, known**

- The genealogist role (`PULL-PROTOCOL.md`) has no holder yet.
- Self-hosted and app versions of the shared-pad surface: V3.1.
- Watcher scripts (the `Watchers` chapter describes the shapes; no scripts ship).

**Why pull, not push.** Each house is sovereign. It doesn't make sense to hand a house "the best version"; it makes sense for the house to look at the current best understanding and take in what it wants, how it wants. When you've pulled, write down what you valued, what you thought, and where you diverged and did better — and send that back (`CONTRIBUTING.md`). The divergences are the most valuable thing we receive.
