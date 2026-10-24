# claude-plugins-marketplace

Personal Claude Code marketplace by **Denis Clairbois**, used to share Claude Code tooling with colleagues without any manual setup on their side.

## Installation

In a Claude Code session, run:

    /plugin marketplace add inteltechsys/claude-plugins-marketplace
    /plugin install bash-course-plugin@denis-marketplace

No token, no special permission required — this repo is public.

## Available plugin: `bash-course-plugin`

Bundles the bash / pentest training workflow tooling developed on the `bash_course_udemy` repo:

### Hooks (`hooks/`)
- **`block-push-main.sh`** (`PreToolUse`, matcher `Bash`) — blocks any direct `git push` to `main`.
- **`check-shellcheck.sh`** (`PostToolUse`, matcher `Edit|Write`) — runs `shellcheck` after every file edit.
- **`save-before-compact.sh`** (`PreCompact`) — saves state before a context compaction.

### Skill (`skills/nouveau-script/`)
- **`nouveau-script`** — assists creating a new bash script following the project's conventions.

### Agent (`agents/`)
- **`bash-reviewer`** — code review agent for bash scripts.

## Repo structure

    claude-plugins-marketplace/
    ├── .claude-plugin/
    │   └── marketplace.json          # "denis-marketplace" manifest
    ├── README.md
    └── plugins/
        └── bash-course-plugin/
            ├── .claude-plugin/
            │   └── plugin.json       # plugin manifest
            ├── hooks/
            ├── skills/
            └── agents/

## Author

Denis Clairbois
