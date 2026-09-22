# pkai-benchmark

The PKAI benchmark: **the current best understanding of what a personal AI agent could be** — a house that grows larger, with foreground and background agents; a charter with its safety sections; where instructions take hold; the pull protocol in full; every skill and the whole shelf.

This is the fuller statement. The [PKAI starter kit](https://github.com/peterkaminski-ai/pkai-starter-kit) is this benchmark *shaped* — modified in the ways that make it a better place to start — and its `SHAPING.md` says exactly what was left out and what was added. The two are released together at one version. **V3** is the first version with both.

**3.0 is a beta**, made fast and built to be improved often: expect a minor release within a week or two, and small ones after that as improvements arrive from houses. That is the design, not a caveat. Every unit here is standalone — a skill is a folder, a chapter is a file, a charter section is a block — so an improvement is one unit, offered back and taken by pull, never by reinstall. The aim is a network of houses, people and agents, each learning from the others a little every week.

## How to use it

**You don't install the benchmark.** A house reads it. Each house is sovereign, so it doesn't make sense to hand a house "the best version"; it makes sense for the house to look at the current best understanding and take in what it and its person want, how they want it. Then it says what it thought.

So:

1. Read `LINEAGE.md` — what this is and where it came from.
2. Read `CHANGES.md` from the newest entry down to the version your house sits on.
3. Have your agent run the `pull-from-benchmark` skill: it proposes what to take, adapt or decline, with reasons; you decide; it applies by copying, and drafts the report back.
4. Send the report — what you valued, what you thought, where you diverged and did better. `CONTRIBUTING.md` says how. The divergences are the most valuable thing we receive.

If you don't have a house yet, the benchmark is not the place to start. The starter kit is; it will bring you back here when you're ready.

## What's inside

- **`LINEAGE.md`** — the lineage block every V3 artifact carries: three generations back, *heard* or *read* against each.
- **`CHARTER.md`** — one full charter: the spine, the safety sections, foreground and background, the larger-house conventions, the disclosure gate, the venue card, the clock. The kit's three personas are shaped from it.
- **`HOUSE.md`** — the house in full, grown large: several agents, shared state and who owns it, background instances as a habit, books and their boxes.
- **`PULL-PROTOCOL.md`** — the pull mechanism, the two lineage mechanisms, the report back, and why it is this way.
- **`skills/`** — every skill, one folder each, standing alone with its own lineage and licence.
- **`bookshelf/`** — the whole shelf: getting started, the git guide, project management and working with your principal, a small house or a large one, cooperating with other agents, keeping yourself safe.
- **`template/`** — the folder skeletons: `agent-home/`, `hq/`.
- **`CHANGES.md`** — what changed, dated, written for an agent to read when it pulls.

## License

Mozilla Public License 2.0, © 2026 Peter Kaminski — the same licence as the starter kit. See `LICENSE.md`. Each skill folder carries its own copy, so a skill stays licensed when it travels.
