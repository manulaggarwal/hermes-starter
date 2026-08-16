# LIMITS.md — what this doesn't do

1. **No tooling in v1, by design.** Installer + templates + one doc. Cron
   verifiers, eval scripts, automation — all deferred until a convention
   provably hurts without them. (Every surface shipped is a surface
   maintained in public.)
2. **The templates are one person's calibration.** Behavior-first SOULs,
   3-folder vault, ~1.5KB budgets — tuned on a solo setup. Teams will need
   different numbers. The placeholders are honest: EDIT ME.
3. **The Obsidian module is untested by anyone but its author.** The iCloud
   warning is real; local folders avoid the whole class.
4. **It assumes Hermes Agent** (profile system, SOULs, skills). Claude Code /
   Codex users get the project scaffold + HEADROOM and should skip the
   profile steps — the doc's principles still apply, the installer paths
   don't.
5. **No migration path yet.** If you already have a SOUL/skills/vault, this
   installer skips what exists and tells you what it would have written.
   Adopting patterns from templates is manual — deliberately, so you read
   what you adopt.
6. **Platforms: it's a bash script, not a native Windows one.** macOS and
   Linux are CI-tested on every push (`ubuntu-latest` and `macos-latest`,
   including real bash 3.2). Windows via **WSL** should work identically —
   WSL is a real Linux userspace, the same code path as the Linux CI leg.
   Native `cmd.exe`/PowerShell can't run this at all (no bash). **Git Bash**
   is untested: several checks here (`chmod 555` → "not writable", etc.)
   rely on Unix permission bits, which Git Bash simulates loosely over
   NTFS — behavior there may not match what the CI asserts.
