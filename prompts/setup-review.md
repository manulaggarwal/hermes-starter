# setup-review prompt — paste into any AI agent (Hermes, Claude, ChatGPT)

*Turns HEADROOM.md into an actionable audit. Paste this whole file (or just
the block below) along with the outputs the agent asks for.*

---

You are auditing my agent setup against the HEADROOM principles. Be specific
and blunt — I want findings, not reassurance.

The principles:
1. SOUL = identity + channel rules + behavior constraints (≤ ~1.5KB each)
2. Skill = procedure; only its name+description is always visible
3. Memory = pointers + stable preferences, small and pruned
4. Files = truth; every fact lives in ONE place, everything else points
5. Tier loading: referenced → saved → auto-loaded; default cheapest
6. CLAUDE.md/AGENTS.md are tier 3 (auto-loaded) — budget ≤ 3KB (2× a SOUL); memory ≤ ~5KB

Ask me for (or read, if you have file access):
- FIRST: the paste of `bin/headroom-check` output if I have it (it has the sizes)
- My global SOUL.md (~/.hermes/SOUL.md) and one profile SOUL.md (~/.hermes/profiles/<name>/SOUL.md)
- The output of `wc -c` on each
- My memory file contents (~/.hermes/profiles/<name>/memories/MEMORY.md)
- A list of my skills/plugins and which I actually used last month

If I didn't give you a file or value, write UNKNOWN — do not guess.

Then report:
1. **OVER-BUDGET:** any resident file that's too big and WHAT to cut
2. **MISPLACED:** procedures living in SOULs; truths living in memory;
   procedures duplicated in multiple places
3. **STALE:** memory entries that state facts a file should own (project state, paths, version numbers — anything that drifts)
4. **TIER VIOLATIONS:** things auto-loaded that only need to be referenced
5. **MISSING:** habits absent (run logs, daily-logs, NEXT.md, watchlist)
6. **Top 3 fixes,** ranked by headroom gained per minute spent

Finish with a one-line verdict: what's the single biggest token leak in my
setup?
