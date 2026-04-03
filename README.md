# Claude Code Book Documentation Corpus

A data-only documentation corpus for [Claude Code from Source](https://github.com/alejandrobalderas/claude-code-from-source) by [Alejandro Balderas](https://github.com/alejandrobalderas) — an 18-chapter technical book analyzing the architecture of Anthropic's Claude Code CLI.

Use with the [`hiivmind-corpus`](https://github.com/hiivmind/hiivmind-corpus) plugin for navigation and maintenance.

## About the Source

This corpus indexes **Claude Code from Source**, a reverse-engineered architectural analysis of Claude Code written in the style of an O'Reilly technical book. The book covers:

- The six core abstractions (query loop, tool system, tasks, state, memory, hooks)
- The 1,730-line agent loop and four-layer context compression
- Concurrent tool execution with speculative streaming
- Fork agents as a prompt cache exploitation mechanism
- File-based memory with LLM-powered recall
- Skills, hooks, and MCP extensibility
- Custom terminal renderer running at 60fps
- Remote execution across four topologies

18 chapters, ~6,200 lines of markdown, 25+ Mermaid diagrams.

**Full credit to [Alejandro Balderas](https://github.com/alejandrobalderas) for writing the original book.**

## Quick Start

### 1. Install the hiivmind-corpus plugin

```bash
# In Claude Code
/install-plugin hiivmind/hiivmind-corpus
```

### 2. Register this corpus

```bash
/hiivmind-corpus register github:hiivmind/hiivmind-corpus-claudecodebook
```

### 3. Start asking questions

```
How does the Claude Code agent loop work?
What is the prompt cache architecture?
How does concurrent tool execution work?
How does Claude Code's memory system persist across sessions?
What are fork agents and why do they exist?
```

## Corpus Structure

```
hiivmind-corpus-claudecodebook/
├── config.yaml          # Source definitions, keywords, tracking
├── index.yaml           # Structured index (machine-queryable)
├── index.md             # Rendered index (human-readable)
├── graph.yaml           # Concept graph (9 concepts, 11 relationships)
├── render-index.sh      # Deterministic index.yaml -> index.md renderer
├── .source/             # Cloned source repo (gitignored)
└── README.md
```

## Concept Graph

The corpus is organized into 9 concepts:

| Concept | Chapters | Description |
|---------|----------|-------------|
| Core Architecture | ch01, ch03, ch05, ch18 | Six abstractions, agent loop, state management |
| Tool System | ch06, ch07 | Tool interface, execution pipeline, concurrency |
| Multi-Agent | ch08, ch09, ch10 | Sub-agents, fork agents, tasks, coordination |
| API and Caching | ch04, ch09, ch17 | API layer, prompt cache, performance |
| Memory and Persistence | ch11 | File-based memory, LLM recall, team memory |
| Extensibility | ch12, ch15 | Skills, hooks, MCP protocol |
| Terminal and Input | ch13, ch14 | Custom renderer, keyboard protocols |
| Remote Execution | ch16 | Bridge, Direct Connect, upstream proxy |
| Bootstrap | ch02 | Startup pipeline, trust boundary |

## Maintenance

| Command | Purpose |
|---------|---------|
| `/hiivmind-corpus refresh claudecodebook` | Update from upstream changes |
| `/hiivmind-corpus enhance claudecodebook <topic>` | Add depth to a topic |
| `/hiivmind-corpus build claudecodebook` | Full rebuild |

## Requirements

- [`hiivmind-corpus`](https://github.com/hiivmind/hiivmind-corpus) plugin (provides all operations)
- Git (for source management)

## License

MIT
