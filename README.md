# VideoToText Plugins Marketplace

Public marketplace for **Claude** and **ChatGPT / Codex** plugins.

Website: https://videototext.click  
MCP docs: https://videototext.click/docs/mcp  
API keys: https://videototext.click/settings/api

## Claude (Directory → Plugins → Add marketplace)

1. Choose **Add from a repository**
2. URL:

```text
maksgamal/videototext-plugins
```

3. Click **Sync** → install **VideoToText**
4. Set `VIDEOTOTEXT_API_KEY=ctf_...` and restart Claude

Or in Claude Code:

```text
/plugin marketplace add maksgamal/videototext-plugins
/plugin install videototext@videototext
```

## ChatGPT / Codex

```bash
codex plugin marketplace add maksgamal/videototext-plugins --ref main
codex plugin add videototext@videototext-marketplace
```

Then set `VIDEOTOTEXT_API_KEY=ctf_...` and restart.

## What's included

| Path | Purpose |
|------|---------|
| `.claude-plugin/marketplace.json` | Claude marketplace catalog |
| `.agents/plugins/marketplace.json` | Codex / ChatGPT marketplace catalog |
| `plugins/videototext/` | Plugin (skills + MCP config) |

MCP endpoint uses your VideoToText API key (`x-api-key` header).
