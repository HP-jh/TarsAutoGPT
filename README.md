# TarsAutoGPT

MCP integration for AutoGPT (autonomous AI agent).

## Tools

- `autogpt_status` — Get AutoGPT agent status
- `autogpt_interact` — Send an instruction to AutoGPT

## Quick Start

```bash
go build -o tarsautogpt
TARS_MCP_ENDPOINT=https://api.example.com TARS_MCP_API_KEY=xxx ./tarsautogpt
```

## Environment Variables

- `TARS_MCP_ENDPOINT` — upstream API endpoint
- `TARS_MCP_API_KEY` — upstream API key
- `TARS_MCP_MODE` — `stdio` (default) or `http`

## License

MIT
