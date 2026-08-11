---
name: videototext
description: Fetch, search, summarize, or export a YouTube video transcript with VideoToText MCP. Use when the user pastes a youtube.com or youtu.be URL or asks for captions, summary, chapters, or RAG chunks.
---

# VideoToText

Primary skill for YouTube / video transcripts.

## When to use

- User pastes a YouTube URL (`youtube.com` / `youtu.be`)
- User asks for transcript, captions, subtitles, summary, chapters, or RAG export

## Steps

1. Call MCP tool `cliptext_get_transcript` with the video URL or ID.
2. For summaries, call `cliptext_summarize` (`bullet` | `short` | `long`) and optionally `cliptext_get_chapters`.
3. For search, call `cliptext_search_transcript` with the keyword.
4. For RAG / vector DB, call `cliptext_export_for_rag`.
5. For file formats, call `cliptext_get_formats` (`txt` | `md` | `srt` | `vtt` | `json` | `csv`).

## Output

- Short overview (title, channel, 2–4 sentence summary)
- Timestamped quotes when citing claims (`[mm:ss]`)
- Never invent transcript text — only use MCP tool results

## Auth

MCP requires header `x-api-key` with a `ctf_...` key from https://videototext.click/settings/api  
Env var used by `.mcp.json`: `VIDEOTOTEXT_API_KEY`
