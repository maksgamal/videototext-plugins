# VideoToText Plugins Marketplace

Public marketplace for **Claude** and **ChatGPT / Codex** plugins.

**AI video to text** for YouTube, TikTok, Instagram, Facebook, X, LinkedIn, and Pinterest — searchable transcripts, summaries, chapters, and RAG exports.

Website: https://videototext.click  
MCP docs: https://videototext.click/docs/mcp  
API keys: https://videototext.click/settings/api

## Claude (Directory → Plugins → Add marketplace)

```text
maksgamal/videototext-plugins
```

```text
/plugin marketplace add maksgamal/videototext-plugins
/plugin install videototext@videototext
```

## ChatGPT / Codex

```bash
codex plugin marketplace add maksgamal/videototext-plugins --ref main
codex plugin add videototext@videototext-marketplace
```

Set `VIDEOTOTEXT_API_KEY=ctf_...` and restart.
