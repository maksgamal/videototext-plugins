---
name: get-youtube-transcript
description: Fetch a YouTube or video transcript with timestamps via VideoToText MCP. Use when the user pastes a youtube.com or youtu.be URL, asks for captions/subtitles, or needs the spoken content of a video as text.
---

# Get YouTube transcript

Use this skill whenever the user shares a YouTube URL (`youtube.com` or `youtu.be`) or asks for a video transcript.

## Steps

1. Extract the video URL or video ID from the user message.
2. Call MCP tool `cliptext_get_transcript` with that URL or ID.
3. Present a concise overview:
   - Title and channel
   - Duration / language when available
   - Short summary of what the video covers (2–4 sentences)
4. Keep the full transcript available for follow-up questions; quote with timestamps when citing specific claims.
5. If the tool fails (private video, no captions, credits exhausted), explain the error and suggest a public video or checking API credits at https://videototext.click/settings/api

## Rules

- Do not invent transcript text. Only use tool output.
- Prefer timestamped citations like `[12:34]` when quoting.
- Do not ask the user to paste captions manually if the MCP tool can fetch them.
