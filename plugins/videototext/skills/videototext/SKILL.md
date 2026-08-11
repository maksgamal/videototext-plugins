---
name: videototext
description: Convert YouTube, TikTok, Instagram, Facebook, X, LinkedIn, or Pinterest videos to text with VideoToText MCP. Use when the user pastes a video URL or asks for transcript, captions, summary, chapters, or RAG export.
---

# VideoToText

AI video-to-text for 7 platforms: YouTube, TikTok, Instagram, Facebook, X (Twitter), LinkedIn, and Pinterest.

## When to use

- User pastes a public video URL from any supported platform
- User asks for transcript, captions, subtitles, summary, chapters, or RAG export
- User wants to search a video for a quote or jump to a timestamp

## Steps

1. Call MCP tool `cliptext_get_transcript` with the video URL.
2. For summaries, call `cliptext_summarize` (`bullet` | `short` | `long`) and optionally `cliptext_get_chapters`.
3. For search, call `cliptext_search_transcript` with the keyword.
4. For RAG / vector DB, call `cliptext_export_for_rag`.
5. For file formats, call `cliptext_get_formats` (`txt` | `md` | `srt` | `vtt` | `json` | `csv`).

## Output

- Short overview (title, source, 2–4 sentence summary)
- Timestamped quotes when citing claims (`[mm:ss]`)
- Never invent transcript text — only use MCP tool results

## Auth

MCP requires header `x-api-key` with a `ctf_...` key from https://videototext.click/settings/api  
Env var used by `.mcp.json`: `VIDEOTOTEXT_API_KEY`
