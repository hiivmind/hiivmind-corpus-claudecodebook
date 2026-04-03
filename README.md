# Claude Code Book Documentation Corpus

A data-only documentation corpus for Claude Code Book. Use with the `hiivmind-corpus` plugin for navigation and maintenance.

## What is This?

This repository contains:
- **Indexed documentation** - Structured index of Claude Code Book docs with summaries and cross-references
- **Source tracking** - Configuration tracking upstream documentation commits
- **Keywords** - Routing keywords for automatic corpus selection

This is NOT a Claude Code plugin. All operations (navigation, building, refreshing) are provided by the `hiivmind-corpus` plugin.

## Quick Start

### 1. Install the hiivmind-corpus plugin

```bash
# In Claude Code
/plugin install hiivmind/hiivmind-corpus
```

### 2. Register this corpus

```bash
# Register from GitHub
/hiivmind-corpus register github:hiivmind/hiivmind-corpus-claudecodebook
```

### 3. Start asking questions

```
How do I set up Claude Code from scratch?
What are best practices for using Claude Code effectively?
How does Claude Code handle context management?
```

## File Structure

```
hiivmind-corpus-claudecodebook/
├── config.yaml          # Source definitions, keywords, tracking
├── index.md             # Main documentation index
├── index-*.md           # Sub-indexes (for large corpora)
├── uploads/             # Local document uploads
├── .source/             # Cloned docs (gitignored)
├── .cache/              # Web cache (gitignored)
└── README.md
```

## Maintenance

Use `hiivmind-corpus` skills to maintain this corpus:

| Command | Purpose |
|---------|---------|
| `/hiivmind-corpus refresh claudecodebook` | Update from upstream changes |
| `/hiivmind-corpus enhance claudecodebook <topic>` | Add depth to a topic |
| `/hiivmind-corpus build claudecodebook` | Full rebuild |
| `/hiivmind-corpus add-source claudecodebook <url>` | Add new source |

## config.yaml Schema

```yaml
schema_version: 2

corpus:
  name: "claudecodebook"
  display_name: "Claude Code Book"
  keywords:            # For automatic routing
    - claude code
    - claude code book
    - claude code from source
    - cc from source

sources:
  - id: claudecodebook
    type: git
    repo_url: https://github.com/...
    branch: main
    last_commit_sha: "..."
    last_indexed_at: "..."
```

## Requirements

- `hiivmind-corpus` plugin (provides all operations)
- Git (for source management)

## License

MIT
