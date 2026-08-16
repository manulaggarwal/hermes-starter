# hermes-starter

> **One command. Ten minutes. A complete agent system.**
> `bin/hermes-setup` gives a first-time Hermes Agent user what took months to learn the hard way: an agent that sounds deliberate, writes to files that outlive sessions, picks them back up, and has token headroom from day one.
> Obsidian users: say yes at the prompt, get a wired vault. Everyone else: plain markdown, no lock-in, nothing lost.
> Read [docs/HEADROOM.md](docs/HEADROOM.md) — the one doc that matters.

---

## What it sets up

| Layer | What you get | Where |
|---|---|---|
| **Global SOUL** | Channel rules inherited by every profile (the highest-leverage file in the system) | `~/.hermes/SOUL.md` |
| **Profile SOUL** | Behavior-first template: your stack facts, not generic personality prose | `<profile>/SOUL.md` |
| **Project scaffold** | `CLAUDE.md` + `NEXT.md` + `daily-logs/` + `knowledge/` + `watchlist.md` | your project dir |
| **Obsidian vault** *(optional, prompt-gated)* | 3-folder vault, AGENT.md navigation, canonicality rules, iCloud warning | your vault path |
| **headroom-check** | Measures what HEADROOM teaches: SOUL sizes vs budget, tier-3 context files, memory bloat, habit presence | `bin/headroom-check` |
| **setup-review prompt** | Paste into any AI: audits your setup against the HEADROOM principles | `prompts/setup-review.md` |

Everything is plain markdown you own. Idempotent — re-running never clobbers.

## Quick start

```bash
git clone https://github.com/manulaggarwal/hermes-starter
bash hermes-starter/bin/hermes-setup
# answer 3-4 questions, done
```

Want to see what it would do first? `bin/hermes-setup --dry-run` previews every
write without touching disk. `--profile`/`--project`/`--vault DIR` skip the
matching prompt if you'd rather not type paths interactively; `--help` lists
all of it.

No dependencies. No accounts. No lock-in.

```bash
bash hermes-starter/bin/headroom-check   # measure your setup's token budget
```

## The philosophy (10 lines)

1. **SOUL = identity. Skill = procedure. Memory = pointers. Files = truth.**
2. Every layer of your system spends the agent's attention. Spend it on purpose.
3. One line of real constraint beats five aphorisms.
4. The file wins every conflict; memory points, never copies.
5. Facts that outgrow memory graduate to files.
6. Tier your loading: referenced → saved → auto-loaded. Default cheapest.
7. Log runs: one dated line per outcome. Failures especially.
8. Defer tools with revisit triggers, not vibes.
9. Future-proof = adoptable late, not early.
10. Read HEADROOM.md. Then read it again in week four.

## Pairs with

- **[wronglist](https://github.com/manulaggarwal/wronglist)** — constraint files that make agents more correct over time. When you're ready for evals: `wronglist init`.

## Limits

Honest and full in [LIMITS.md](LIMITS.md) — template calibration, deferred tooling, and what's untested. Read it before adopting.

## License

MIT
