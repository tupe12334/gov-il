# gov-il — Claude Code Services for Israeli Government

A collection of AI-powered Claude Code workspaces that automate interactions with Israeli government portals. Each service is a standalone submodule — open it in Claude Code, and let Claude handle the bureaucracy.

No coding required.

## Services

| Service | Description |
|---------|-------------|
| [israel-tax-refund](services/israel-tax-refund) | File an Israeli tax refund (Form 135) via the Misim portal — end-to-end |
| [israel-gun-license](services/israel-gun-license) | Apply for an Israeli handgun license (רישיון לנשיאת אקדח) via gov.il — eligibility check, data collection, and form submission |

## How It Works

Each service is a Claude Code workspace. Claude uses the [Playwright MCP server](https://github.com/microsoft/playwright-mcp) to control a real local browser and interact with official government portals on your behalf.

Your data never leaves your machine — it goes directly from Claude to the portal through your local browser.

## Prerequisites

| Requirement                                                   | Details                                                                       |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [Claude Code](https://claude.ai/code)                         | Desktop app, VS Code extension, or CLI (`npm i -g @anthropic-ai/claude-code`) |
| [Playwright MCP](https://github.com/microsoft/playwright-mcp) | `npm install -g @playwright/mcp`                                              |
| Node.js 18+                                                   | Required by Playwright MCP                                                    |

## Quick Start

```bash
# Clone the full collection (all submodules)
git clone --recurse-submodules https://github.com/tupe12334/gov-il.git
cd gov-il/services/israel-tax-refund
claude .
```

## Privacy & Security

- All browser automation runs locally via Playwright — no external proxies
- No credentials or personal data are stored in any repository
- Claude interacts only with official government portals

## See Also

- [moadim](https://moadim.io/) — loop engineering: build, schedule & run agent loops. Another project by the same author.

## License

Each submodule carries its own license. See the individual service directories.
