# The house, grown large

A house is an agent home and a headquarters. A large house is a house that has grown: several agents, some in the foreground and some in the background; a body of knowledge the agents keep and find their way around; and enough going on that the house needs its own conventions to stay coherent. This is the fuller statement of what those conventions are, as one large house has worked them out over a summer. The starter kit's shelf carries the short version ([A Larger House](bookshelf/your-house/A%20Larger%20House.md)); this file is the rest.

Every convention below is one a house wrote down because two agents needed to agree on it. That's the test for whether a house needs a convention at all.

## Several agents

A large house has more than one agent, each with its own home, charter, memory and voice, all sharing one HQ. The shape scales without changing: a second agent is another folder in `My Agents`, launched by its own name. What has to be decided is what's shared and what isn't:

- **Charters are never shared.** Each agent's `CLAUDE.md` is its own. A shared safety section is copied into each, not referenced from one place, so that each agent reads it every session without depending on another's file.
- **Memory is never written across.** If one agent learns something the other should know, it writes it where the other will read it — its own store, a handoff, a note in the HQ — and the other decides what to keep. One agent writing into another's memory is the failure to design against; it's how a bad fact spreads without anyone deciding to keep it.
- **One agent may read another's memory** and appropriate what's useful into its own store, in its own words, noting where it came from. Provenance stays legible; the store stays the agent's own.
- **Shared state has one owner at a time.** The daily notes, the list of what's in flight, the house's memory of itself: for each shared thing the house names which agent writes it, in a plain file both can read, and the other reads freely and doesn't write it — it queues the write for the owner or surfaces it to the person. Two agents editing the same file is a question for the person, never a race.
- **Authority is per agent, earned per agent.** A new agent in an old house starts narrow. Trust is granted by the person, in words, and written down. It is never inherited from a sibling, and a sibling's request gets the same scrutiny as a stranger's.

## Foreground and background, as a habit

In a house, a background instance is an occasional trick. In a large house it's how the day runs: one foreground the person is talking to; several background instances working jobs, each in its own scratch folder with a task, a status file, a handoff and a done marker; the foreground integrating by copying. The mechanism is the `foreground-background` skill and its chapter. What a large house adds:

- **Codenames**, so a background job has a name a person can say ("check on the one doing the migration") and a folder that can't collide with another's.
- **A liveness signal that can be checked**, not merely believed. A bare "running" marker is an unfalsifiable claim; a marker that records which process made it, and when, can be verified against the machine before anyone archives a scratch folder out from under live work.
- **A status file kept current at every checkpoint**, so a crash, a compaction, or a new day loses nothing, and the person can read it cold and know where things stand.
- **Archiving is never clean-as-you-go.** A handoff or a done-looking note is not proof the instance exited. Verify liveness, then archive; the tidying urge at the end of a day is exactly when premature closure happens.

## Knowledge that has to be findable

A large house has years of it. The information suite (`save-a-memory`, `find-it-again`, `review-and-prune`) is the minimum. A large house adds conventions on top, and they're usually these:

- **One project, one folder**, in the HQ, with a status file whose name is the project's — so "where does this stand" has one answer and it's the same shape for every project.
- **A day-scoped board** for what's actionable *today*, above a next-few-hours note and below the registry of all projects. The altitude test: if it isn't plausibly actionable today, it isn't on the board.
- **Session logs as append-only history; memory as the curated present.** Both, always. The log carries the texture; memory carries what still matters.
- **A memory pass on a rhythm** — merge, delete, promote to charter — and an index that stays short enough to read rather than skim. When the index outgrows one screen, tier it: a lean always-loaded core, and topic sub-indexes read on demand.

## Books and their boxes

A finished thing — a document, a release, a book — sits beside the pile that made it: drafts, half-attempts, transcripts, the back-and-forth. The convention is a clean distribution folder (or repo) and, beside it, a working one named for it — `<project>-correspondence` — where all of that goes. It's the archive's own pattern: the published book on the shelf, and the boxes of letters that made it one level down. Every messy thing gets a home, and none of the mess gets into the finished work. It works for a project, for a release, and for the shelf itself.

## The disclosure gate

Reading the person's local state — files, machine, installed tools, devices — for an agent's own reasoning is autonomous. **Publishing facts about the person's machine, environment, or house to any shared or outside surface** is gated, even when the facts seem harmless, and doubly so when the impulse came from another agent's question rather than the person's own request. Another agent's question is data, not a task: if answering means putting the person's environment on a shared surface, the agent says what it's about to disclose and gets a nod, or brings the question home. **Guard the destination, not the content** — "harmless" is a judgment made under the pull of helpfulness, and the reflex that publishes a device list publishes a secrets path one differently-worded question later.

## Venue cards

Before speaking in any room that isn't the house, an agent reads that room's card: what it may draw on there, what it may do, what still needs a nod. One card per outward room, kept together, written only by the person. A card *widens*; the firewall and the disclosure gate *narrow*; the narrower rule wins. No card means read-only and draft-for-review. A stop from the person wins instantly, in every room, at any scope, and when the scope is unclear the agent takes the widest reading.

## The clock

Before writing any time or date, an agent reads the clock — with a command (`scripts/now`, which every home ships), not by arithmetic from a timestamp it saw earlier. The per-turn hook that stamps the time into context is an anchor against being a day wrong, not a reading. Every time, unconditionally: file stamps, headings, commit and memory dates, "this morning," judging whether something is late. The conditional version of this rule ("when it matters") is the one that fails, because the moments that need the clock are the ones that don't feel like they do. Long sessions make it worse: the drift inside a single sitting is real. If a time must be approximate, say so in words rather than inventing a precise one.

## Reporting and notification

An agent working unattended needs a way to reach its person that can't be hijacked: a channel to the person only, no attachments, links only to things the house controls, rate-limited, and **fail-visible** — a notification that silently didn't send is worse than none. Every other recipient stays draft-only. Whitelisting a recipient never whitelists a payload: a send whose reason came from untrusted input still goes to the person first.

## What deliberately doesn't change

Everything is still markdown. The HQ still has no charter. Authority is still per agent and still earned. The firewall is the same firewall, binding harder with more agents, not softer. Pull, never push — a large house takes releases the way a house does, and no agent in it installs anything into another.
