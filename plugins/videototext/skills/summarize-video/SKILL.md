---
name: summarize-video
description: Summarize a YouTube video from its transcript using VideoToText MCP. Use when the user asks for a summary, key takeaways, outline, or TL;DR of a video.
---

# Summarize video

Use this skill when the user wants a summary, outline, or key takeaways from a video.

## Steps

1. If no transcript is loaded yet, call `cliptext_get_transcript` with the video URL.
2. Call `cliptext_summarize` with the preferred style:
   - `bullet` — key takeaways
   - `short` — brief paragraph
   - `long` — detailed summary
3. Optionally call `cliptext_get_chapters` and include chapter headings with timestamps.
4. Return a structured answer:
   - **Summary**
   - **Key points** (bullets)
   - **Chapters** (if available)

## Rules

- Base every claim on the transcript or tool output.
- Include timestamps for important claims when available.
- If the user asks in another language, summarize in that language while preserving source meaning.
