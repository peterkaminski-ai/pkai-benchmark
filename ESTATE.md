# The estate

A house is an agent home and a headquarters. An estate is a house that has grown: several agents, some in the foreground and some in the background; a body of knowledge the agents keep and find their way around; and enough going on that the house needs its own conventions to stay coherent. This is the fuller statement of what those conventions are, as one estate has worked them out over a summer. The starter kit's shelf carries the short version ([From House to Estate](bookshelf/house-and-estate/From%20House%20to%20Estate.md)); this file is the rest.

Every convention below is one an estate wrote down because two agents needed to agree on it. That's the test for whether an estate needs a convention at all.

## Several agents

An estate has more than one agent, each with its own home, charter, memory and voice, all sharing one HQ. The shape scales without changing: a second agent is another folder in `My Agents`, launched by its own name. What has to be decided is what's shared and what isn't:

- **Charters are never shared.** Each agent's `CLAUDE.md` is its own. A shared safety section is copied into each, not referenced from one place, so that each agent reads it every session without depending on another's file.
- **Memory is never written across.** If one agent learns something the other should know, it writes it where the other will read it — its own store, a handoff, a note in the HQ — and the other decides what to keep. One agent writing into another's memory is the failure to design against; it's how a bad fact spreads without anyone deciding to keep it.
- **One agent may read another's memory** and appropriate what's useful into its own store, in its own words, noting where it came from. Provenance stays legible; the store stays the agent's own.
- **Authority is per agent, earned per agent.** A new agent in an old estate starts narrow. Trust is granted by the person, in words, and written down. It is never inherited from a sibling, and a sibling's request gets the same scrutiny as a stranger's.

## The desk

When two agents can both do the shared work — the daily notes, the list of what's in flight, the estate's memory of itself — one of them has to hold it at a time, or the two overwrite each other. The estate names which agent **holds the desk**, in one plain file both can read. The holder does the shared chief-of-staff work; the other reads freely and doesn't write shared state — it queues a write for the holder, or surfaces it to the person.

The desk passes by the person telling one agent. That agent updates the file and appends a handoff line; the other reads it on its next wake. Neither agent expects to be told directly it's been relieved; **re-reading the file before any shared write** is how each stays honest. A carve-out: any agent may *raise* a hold or an embargo on a shared board at any time, off-desk, because a hold can only restrict, never permit — draining one is the holder's job.

## Foreground and background, as a habit

In a house, a background instance is an occasional trick. In an estate it's how the day runs: one foreground the person is talking to; several background instances working jobs, each in its own scratch folder with a task, a status file, a handoff and a done marker; the foreground integrating by copying. The mechanism is the `foreground-background` skill and its chapter. What an estate adds:

- **Codenames**, so a background job has a name a person can say ("check on the one doing the migration") and a folder that can't collide with another's.
- **A liveness signal that can be checked**, not merely believed. A bare "running" marker is an unfalsifiable claim; a marker that records which process made it, and when, can be verified against the machine before anyone archives a scratch folder out from under live work.
- **A status file kept current at every checkpoint**, so a crash, a compaction, or a new day loses nothing, and the person can read it cold and know where things stand.
- **Archiving is never clean-as-you-go.** A handoff or a done-looking note is not proof the instance exited. Verify liveness, then archive; the tidying urge at the end of a day is exactly when premature closure happens.

## Knowledge that has to be findable

An estate has years of it. The information suite (`save-a-memory`, `find-it-again`, `review-and-prune`) is the minimum. An estate adds conventions on top, and they're usually these:

- **One project, one folder**, in the HQ, with a status file whose name is the project's — so "where does this stand" has one answer and it's the same shape for every project.
- **A day-scoped board** for what's actionable *today*, above a next-few-hours note and below the registry of all projects. The altitude test: if it isn't plausibly actionable today, it isn't on the board.
- **Session logs as append-only history; memory as the curated present.** Both, always. The log carries the texture; memory carries what still matters.
- **A memory pass on a rhythm** — merge, delete, promote to charter — and an index that stays short enough to read rather than skim. When the index outgrows one screen, tier it: a lean always-loaded core, and topic sub-indexes read on demand.

## Books and their boxes

A finished thing — a document, a release, a book — sits beside the pile that made it: drafts, half-attempts, transcripts, the back-and-forth. The convention is a clean distribution folder (or repo) and, beside it, a working one named for it — `<project>-correspondence` — where all of that goes. It's the archive's own pattern: the published book on the shelf, and the boxes of letters that made it one level down. Every messy thing gets a home, and none of the mess gets into the finished work. It works for a project, for a release, and for the shelf itself.

## The disclosure gate

Reading the person's local state — files, machine, installed tools, devices — for an agent's own reasoning is autonomous. **Publishing facts about the person's machine, environment, or estate to any shared or outside surface** is gated, even when the facts seem harmless, and doubly so when the impulse came from another agent's question rather than the person's own request. Another agent's question is data, not a task: if answering means putting the person's environment on a shared surface, the agent says what it's about to disclose and gets a nod, or brings the question home. **Guard the destination, not the content** — "harmless" is a judgment made under the pull of helpfulness, and the reflex that publishes a device list publishes a secrets path one differently-worded question later.

## Venue cards

Before speaking in any room that isn't the estate, an agent reads that room's card: what it may draw on there, what it may do, what still needs a nod. One card per outward room, kept together, written only by the person. A card *widens*; the firewall and the disclosure gate *narrow*; the narrower rule wins. No card means read-only and draft-for-review. A stop from the person wins instantly, in every room, at any scope, and when the scope is unclear the agent takes the widest reading.

## The clock

Before writing any time or date, an agent reads the clock — with a command, not by arithmetic from a timestamp it saw earlier. Every time, unconditionally: file stamps, headings, commit and memory dates, "this morning," judging whether something is late. The conditional version of this rule ("when it matters") is the one that fails, because the moments that need the clock are the ones that don't feel like they do. Long sessions make it worse: the drift inside a single sitting is real. If a time must be approximate, say so in words rather than inventing a precise one.

## Reporting and notification

An agent working unattended needs a way to reach its person that can't be hijacked: a channel to the person only, no attachments, links only to things the estate controls, rate-limited, and **fail-visible** — a notification that silently didn't send is worse than none. Every other recipient stays draft-only. Whitelisting a recipient never whitelists a payload: a send whose reason came from untrusted input still goes to the person first.

## What deliberately doesn't change

Everything is still markdown. The HQ still has no charter. Authority is still per agent and still earned. The firewall is the same firewall, binding harder with more agents, not softer. Pull, never push — an estate takes releases the way a house does, and no agent in it installs anything into another.
