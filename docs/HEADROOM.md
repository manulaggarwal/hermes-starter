# Headroom — token budget for agent systems

*The one doc to read. Your agent has a fixed budget of attention per session.
Every layer of your system spends it: SOULs, skills, memory, files. Spend it
on purpose or lose it to noise. This doc is how to spend it on purpose.*

## The split (memorize this table)

| Layer | Holds | Budget | Test |
|---|---|---|---|
| **SOUL.md** | Identity + channel rules + behavior constraints | ≤ ~1.5KB per profile | "Would this sentence be true for ANY agent? Delete it." |
| **Skills** | Procedures (how to do X) | Description in the index; body loads on demand | Frontmatter: `name` + `description`, strict — it's the contract future tools index |
| **Memory** | Pointers + preferences (stable facts about the user) | Small, pruned | "If a fact outgrows memory, it graduates to a file." |
| **Files** | Truth: docs, decisions, logs, evals | Unlimited on disk — **but CLAUDE.md/AGENTS.md-type files are tier 3 (auto-loaded): budget them like a SOUL** | The file wins every conflict. Memory points; it never copies. |

**Check yourself:** `wc -c SOUL.md` — want < ~1500. If it's over, something
in there is a procedure or an aphorism.

**Why SOUL is not the place for procedures:** everything resident in the
system prompt is paid on *every* session. A procedure belongs in a skill that
loads when needed. One line of real constraint beats five aphorisms —
aphorisms cost the same tokens and change nothing.

## Three-tier loading (what lives where)

1. **Referenced** — a link/path. Costs nothing until used. Default tier.
2. **Saved** — exists locally, mentioned when needed. Never auto-resident.
3. **Auto-loaded** — in the system prompt every session. The most expensive
   real estate you own. Reserve for: identity, channel rules, hard constraints.

Before promoting anything to tier 3, ask: *does this need to auto-trigger,
or just be available?* Default to the cheapest tier that works.

## Run logs (the 10-second habit)

After any significant outcome — success OR failure — one dated line in the
tool/skill's own file:

```
## Run Log
- 2026-08-16: <tool> → <what it did> → <outcome + one lesson>
```

Ten seconds now; six months later you have outcome data no description field
can give you. Log the failures especially — that's the data you'll want.

## Watch lists (deferring without FOMO)

Not adopting a tool? Record it with **revisit triggers** — measurable
conditions that reopen the decision. "Interesting, later" becomes "later,
when X" — and X is a checkbox, not a vibe. Future-proof = adoptable late,
not early: keep contracts strict so future adoption is a script, not a rebuild.

## Canonicality (one truth per fact)

Every fact lives in exactly ONE place. Everything else points at it.
- Repo beats vault. File beats memory. Copy-pasted lists desync — they always
  have, they always will. One canonical file + pointers everywhere else.

## When a fact outgrows memory

1. Write it to a file (knowledge/, the project repo, wherever it belongs)
2. Leave a one-line pointer in memory
3. Prune the original

A small, dense memory beats a large, stale one — for you AND for every
session that has to load it.

## The week-one checklist

- [ ] Global SOUL written (channel rules, inherited everywhere)
- [ ] Profile SOUL edited: real stack facts, not placeholders
- [ ] daily-logs/ started — one paragraph today beats a perfect format never
- [ ] NEXT.md current at end of every session
- [ ] Read this doc again in week four — different lines will apply
