# TarsAutoGPT

TSG (TarsSecureGuard) MCP adapter for **AutoGPT** — Autonomous AI agent platform.

This is one of the **15 MCP integration projects** under github.com/HP-jh/, designed to be:

- **One-click downloadable** from TSG's MCP Marketplace
- **One-click enableable** in the TSG gateway
- **Independently versioned** (this repo) with its own release cycle
- **Tightly integrated** with TSG via the standard MCP protocol

## Quick Start

### Standalone

```bash
# Download from GitHub Releases
curl -L -o tars-autogpt https://github.com/HP-jh/TarsAutoGPT/releases/latest/download/tars-autogpt-$(uname -s | tr A-Z a-z)-amd64
chmod +x tars-autogpt
./tars-autogpt --upstream-endpoint <your-AutoGPT-endpoint>
```

### Via TSG MCP Marketplace

1. Open TSG admin → **MCP Marketplace**
2. Find **TarsAutoGPT** in the list
3. Click **Download** → wait for completion
4. Click **Enable** → enter your AutoGPT endpoint
5. The MCP server is now available to all TSG clients

## MCP Tools Exposed

| Tool | Description |
|------|-------------|
| `autogpt_list_models` | List available AutoGPT models |
| `autogpt_invoke` | Invoke AutoGPT with prompt + params |
| `autogpt_health` | Health check of upstream connection |
| `autogpt_status` | Current TSG integration status |

## Configuration

Configurable via env vars or `~/.tars/autogpt/config.json`:

- `TARS_AUTOGPT_ENDPOINT` — upstream endpoint URL
- `TARS_AUTOGPT_API_KEY` — upstream API key (optional, for hosted services)
- `TARS_AUTOGPT_TIMEOUT` — request timeout (default 30s)
- `TARS_AUTOGPT_LOG_LEVEL` — log verbosity (default info)

## Version

- **v0.1.0** — Initial MVP (basic MCP adapter)
- See [Releases](https://github.com/HP-jh/TarsAutoGPT/releases) for full changelog

## Cross-Repo Coordination

This repo is part of the **15 MCP integration projects** in github.com/HP-jh/. See [HP-jh/TarsSecureGuard](https://github.com/HP-jh/TarsSecureGuard) for the master gateway that orchestrates all 15.

## License

MIT — see [LICENSE](LICENSE).
