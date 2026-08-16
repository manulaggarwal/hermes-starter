# CLAUDE.md — hermes-starter

## What this is
A starter pack for first-time Hermes Agent users: one installer, ten
templates, one doc (HEADROOM.md). NOT a framework — conventions, not tooling.

## Owner
Manul — solo dev. Hermes Agent power user (16+ profiles). Stack: bash 3.2
must stay supported (macOS default), no npm dependency for v1.

## Canonicality
This repo is the source of truth. The Obsidian vault mirrors. Repo wins.

## Locked decisions (v0.1, from concept review)
- Obsidian = optional prompt-gated module, OFF the happy path
- No cron/evals tooling in v1 (wronglist owns evals)
- No EVALS.md template here (one-way arrow to wronglist)
- bash 3.2 compatible; idempotent; never clobber

## Current phase
v0.4.2: 11 review rounds; write layer refactored to one atomic write_tpl
helper, now also covering daily-log's sed-substituted write. Added
--dry-run/--help/--profile/--project/--vault flags, consolidated repeated
type/writability checks into predicate helpers. CI runs the full suite on
macos-latest (real bash 3.2, not just a syntax check) plus shellcheck on
ubuntu-latest, actions/checkout@v5. .gitattributes forces LF so Windows
checkouts can't corrupt the shebang; platform support (macOS/Linux
CI-tested, WSL should work, Git Bash untested, no cmd/PowerShell) is
documented honestly in LIMITS.md. Next: friend validation round — v0.5
comes from what confused them.
