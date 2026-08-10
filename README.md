# MiniCode

A lightweight terminal coding assistant for local development workflows.

MiniCode provides a Claude Code-like agent loop in a compact, readable codebase — suitable for learning, experimentation, and custom tooling.

## Core Capabilities

- Multi-step tool execution: `model → tool → model` loop in a single turn
- Full-screen TUI with transcript scrolling, slash commands, and approval flows
- Per-project session persistence with resume, rename, fork, and compact
- Provider-usage-first context accounting with auto-compact and context collapse
- Built-in tools: file ops, grep, edit, run command, web fetch/search, ask user
- Local Skills (`SKILL.md`) and MCP tools/resources/prompts over stdio or HTTP
- Review-before-write file edits with path and command permission checks
- Oversized tool results stored on disk with a short preview in context

## Installation

```bash
cd mini-code
npm install
npm run install-local
```

The installer asks for the model name, `ANTHROPIC_BASE_URL`, and `ANTHROPIC_AUTH_TOKEN`. Config is stored in `~/.mini-code/`.

## Quick Start

```bash
# Run the installed launcher
minicode

# Development mode
npm run dev

# Offline demo mode
MINI_CODE_MODEL_MODE=mock npm run dev
```

## Common Commands

| Command | Description |
|---------|-------------|
| `/help` | Show interactive help |
| `/tools` | List available tools |
| `/skills` | List discovered skills |
| `/mcp` | Show MCP connection status |
| `/status` | Show session and context status |
| `/init` | Scaffold `.mini-code/` and `MINI.md` |
| `/memory` | Inspect layered memory files |
| `/model` | Inspect or switch model |
| `/resume` | Open session picker |
| `/compact` | Manually compact context |

Management commands: `minicode mcp ...` and `minicode skills ...`.

## Development

```bash
npm run check   # Type check
npm test        # Run tests
```

## License

MIT
