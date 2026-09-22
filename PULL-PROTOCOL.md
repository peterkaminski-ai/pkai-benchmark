# The pull protocol

How a new release of the benchmark reaches a house, and why it is this way and not the obvious way.

## The rule

**Benchmark-and-pull, never push-and-replace.** A new release is published. Each house reads it, takes in what it and its person judge good, in the way they judge good, and reports back. Nothing is ever installed into a house from outside; no migration runs; no house is "upgraded."

## The reason

The obvious reason is breakage: each house has modified its agent, and an upgrade pushed in would overwrite the modifications. That reason is true and it is not the reason.

The reason is **sovereignty**. Each house is its own sovereign whole. It doesn't make sense to give a sovereign house the best version of itself; it makes sense for the house to look at the best current understanding and accept in what it wants, how it wants. A careful migration script would solve the breakage. It cannot honour the sovereignty — and a house that has been carefully migrated has still had something done *to* it. This is written down here so that nobody later "fixes" the friction of pulling with automation and thinks they've kept the design.

The same rule, from the other side: pushing a release into a house is the exercise of authority in that house without its consent. Whatever a house's own rules say about authority, that is not ours to exercise.

## The loop

Pull is half of it. The other half runs back up:

1. **What we valued.** The items taken, and why they helped.
2. **What we thought.** Reactions, confusions, what read wrong.
3. **Where we diverged and did better.** *"We didn't implement it the way the benchmark did. We improved it."*

The third is the most valuable inbound signal a release gets, and a push-and-replace design destroys exactly it — it overwrites the divergence before anyone has looked at it. The `pull-from-benchmark` skill drafts the report; `CONTRIBUTING.md` says where it goes. If the divergence is good, the benchmark takes it at the next release, and the kit takes it from the benchmark at the next shaping. Lessons arrive in the benchmark first; the kit never leads it.

## What a house does, concretely

The `pull-from-benchmark` skill is the procedure. In outline: read the new `LINEAGE.md` and `CHANGES.md` down to the version the house sits on; make one row per change; propose *take / adapt / decline / already better* with a reason each; the person decides; apply only what was decided, by copying, with charter changes drafted for the person to install by hand; update `LINEAGE.md`'s `sits_on`; log it; draft the report. A declined item is decided — it's noted in `LINEAGE.md` so future pulls skip it unless the person reopens it.

## The two lineage mechanisms

**Every object remembers a little.** Each artifact — the benchmark, the kit, each skill, each book — carries a `LINEAGE.md` that points back at least three generations and says, for each, whether that's *heard* or *read*. This ships in every artifact and every house copies it. It costs one file.

**A few remember a lot.** Separately, some people or houses keep genealogies: a full tree from their own vantage point, knowing other trees exist and differ, saying why they keep theirs the way they do. Each house charts its own tree as faithfully as it can, so credit is traceable and the relationships between houses are too. Nobody is obliged to be a genealogist; the network is better when a few are.

Kept deliberately separate: they have different owners (every object; specific people), different costs, and different failure modes. Collapsing them into one "provenance system" would lose the cheap universal one to the expensive rare one.

## Thanks, never a debt

On top of both mechanisms sits a practice, not a rule: value flows back. If your grandfather planted the tree you're eating from, you don't want him out in the cold while you enjoy the fruit. What that looks like is up to each house — thanks, credit, a contribution, a share of what something earned — and the `thanks_to` field in every lineage block says where it would go. It's unobligated. Writing it into the protocol as an obligation would make it a tax, and a tax is not thanks.

## A note on provenance

Lineage is descent — what this grew out of, by generations, and what will grow out of it. Provenance is the narrower thing: for one entry, how we know — *heard* from a person, with a date, or *read* in a record. The lineage block carries both, one word per meaning. Mark provenance at the point a thing enters the record — *transcribed, unverified* versus *confirmed by a participant* — because a machine transcript is a guess, and an argument built on one transcribed word is an argument built on a guess. It costs a tag and it makes the difference visible to the next reader, human or agent, instead of invisible.
