# <Vault name>

Your agent's durable memory, rendered nicely. This folder is plain markdown —
if you ever quit Obsidian, everything still works.

## Folders
- `01-Projects/` — per-project navigation (AGENT.md lives here)
- `02-Knowledge/` — topics that outlive projects
- `03-Daily/` — optional vault-side journaling. NOTE: projects keep their own
  `daily-logs/` — that stays canonical for project work (repo > vault)

## Canonicality
Where a project has a git repo, THE REPO WINS. This vault mirrors and
navigates; it never becomes the second source of truth.

## iCloud warning
If this vault syncs via iCloud: turn OFF "Optimize Mac Storage" for it.
Placeholder eviction + agent writes during sync = corrupted files.
