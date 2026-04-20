# Contributing — gov-il

## Adding a New Service

Each service lives in its own Git repository, added here as a submodule under `services/`.

### Required Files

| File | Purpose |
| --- | --- |
| `README.md` | English documentation — what it does, prerequisites, setup, usage, privacy, troubleshooting, disclaimer, license |
| `README.he.md` | Hebrew translation of README.md |
| `RESOURCES.md` | Links to official portals, regulations, and technical references relevant to the service |
| `LICENSE` | PolyForm Noncommercial License 1.0.0 — copy verbatim from `services/israel-tax-refund/LICENSE` |
| `.mcp.json` | MCP server configuration for Claude Code (at minimum: Playwright MCP) |

### Required Skills

Each service must expose Claude Code skills covering the full automation flow (stored in `.claude/`):

- **Main orchestrator** — entry point, guides the user end-to-end
- **Data collection** — step-by-step interview to gather required information
- **Submission** — Playwright-driven flow that performs the actual portal interaction

Use `services/israel-tax-refund/.claude/` as the reference implementation.

### Adding the Submodule

```bash
git submodule add https://github.com/tupe12334/[repo-name].git services/[service-name]
git commit -m "feat: add [service-name] as submodule"
```

## License

All services use [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/). Do not modify it.
