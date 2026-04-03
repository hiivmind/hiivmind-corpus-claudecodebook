# Claude Code Book Documentation Index

> Sources: 1 | Entries: 18 | Generated: 2026-04-03T12:00:00Z
> Generated from `index.yaml` — do not edit directly

---

## Guide

- **Concurrent Tool Execution** `claude-code-from-source:ch07-concurrency.md` - Partition algorithm for concurrent vs serial tool batches, batch execution with bounded concurrency, StreamingToolExecutor for speculative execution during model streaming, order-preserving result harvesting, and the interrupt behavior contract
- **Extensibility -- Skills and Hooks** `claude-code-from-source:ch12-extensibility.md` - Skills as two-phase loaded markdown commands from seven sources, hooks as lifecycle interceptors at 27+ events with four user-configurable types, snapshot security model, exit code semantics, and skill-hook integration
- **Fork Agents and the Prompt Cache** `claude-code-from-source:ch09-fork-agents.md` - Fork agents as prompt cache exploitation mechanism: byte-identical prefix trick (threaded system prompt, exact tool passthrough, placeholder results), recursive fork prevention, sync-to-async transition, auto-backgrounding, and cache economics
- **Input and Interaction** `claude-code-from-source:ch14-input-interaction.md` - Key parsing pipeline from raw bytes to actions: tokenizer with 50ms timeout, five terminal protocol parsers (CSI u/Kitty, xterm modifyOtherKeys, legacy VT, SGR mouse, bracketed paste), keybinding system with 16 contexts, chord state machine, and vim mode ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **Memory -- Learning Across Conversations** `claude-code-from-source:ch11-memory.md` - File-based memory system with four-type taxonomy (user, feedback, project, reference), two-step write protocol, LLM-powered recall via Sonnet side-query, staleness warnings, team memory with path traversal defense, KAIROS mode daily logs, and background extraction
- **Performance -- Every Millisecond and Token Counts** `claude-code-from-source:ch17-performance.md` - Five performance dimensions: startup latency (module-level I/O, API preconnection), token efficiency (8K default output slot, tool result budgeting), API cost (prompt cache architecture, sticky latches), rendering throughput, and search speed (bitmap pre-filters) ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **Remote Control and Cloud Execution** `claude-code-from-source:ch16-remote.md` - Four remote execution topologies: Bridge v1 (poll-based), Bridge v2 (direct sessions with SSE), Direct Connect (local WebSocket server), and Upstream Proxy (credential injection in containers). Covers asymmetric read/write channels, echo deduplication, and protobuf hand-encoding ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **Spawning Sub-Agents** `claude-code-from-source:ch08-sub-agents.md` - AgentTool definition with dynamic schema, 15-step runAgent lifecycle, six built-in agent types, model resolution chain, feature gating with 12+ flags, and the call() decision tree routing fork/builtin/custom agents ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **Starting Fast -- The Bootstrap Pipeline** `claude-code-from-source:ch02-bootstrap.md` - Five-phase startup pipeline under 300ms budget: fast-path dispatch, module-level I/O parallelism, trust boundary, parallel setup, and seven launch paths converging in replLauncher
- **State -- The Two-Tier Architecture** `claude-code-from-source:ch03-state.md` - Mutable process singleton (STATE, ~80 fields) for infrastructure and minimal reactive store (34-line Zustand-like) for UI, connected by centralized onChange side effects. Covers sticky latches, context building, and cost tracking
- **Talking to Claude -- The API Layer** `claude-code-from-source:ch04-api-layer.md` - Multi-provider client factory, system prompt construction with dynamic boundary marker for cache optimization, streaming with idle watchdog, three-tier prompt caching, and the queryModel generator with retry strategies
- **Tasks, Coordination, and Swarms** `claude-code-from-source:ch10-coordination.md` - Task state machine (7 types, 5 statuses), communication patterns (foreground generator chain, background disk/notifications/messages), coordinator mode, swarm teams with SendMessage routing, and multi-agent topologies ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **The Agent Loop** `claude-code-from-source:ch05-agent-loop.md` - The 1,730-line query() async generator: loop body, four context compression layers (tool result budget, snip compact, microcompact, auto-compact), model streaming with withholding pattern, error recovery escalation ladder, token budgets, and stop hooks
- **The Architecture of an AI Agent** `claude-code-from-source:ch01-architecture.md` - Six core abstractions (query loop, tool system, tasks, state, memory, hooks), the golden path from keystroke to output, permission system with seven modes, multi-provider architecture, and build system
- **The Terminal UI** `claude-code-from-source:ch13-terminal-ui.md` - Custom terminal renderer forked from Ink: custom DOM with seven element types, React Fiber reconciler in ConcurrentRoot mode, seven-stage rendering pipeline with cell-level diffing, double-buffer rendering, and pool-based memory management for zero-GC frames ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **What We Learned** `claude-code-from-source:ch18-epilogue.md` - Five architectural bets (generator loop, file-based memory, self-describing tools, fork cache sharing, hooks over plugins), patterns that transfer vs scale-specific patterns, complexity cost analysis, and future directions for agentic systems

## Reference

- **MCP -- The Universal Tool Protocol** `claude-code-from-source:ch15-mcp.md` - Model Context Protocol implementation: eight transport types (stdio, HTTP, SSE, WebSocket, SDK, IDE, proxy), seven configuration scopes, tool wrapping to native Tool interface, OAuth with RFC discovery and XAA, in-process transport, connection management, and timeout architecture ⚡ GREP - `grep -n '^## \|^### ' FILE`
- **Tools -- From Definition to Execution** `claude-code-from-source:ch06-tools.md` - The Tool interface with three type parameters, buildTool() fail-closed defaults, 14-step execution pipeline, seven permission modes with resolution chain, tool deferred loading, result budgeting, and individual tool highlights (Bash, Edit, Read, Grep, Agent)

---

*Rendered from index.yaml at 2026-04-03T12:00:00Z*
