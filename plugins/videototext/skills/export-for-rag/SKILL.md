---
name: export-for-rag
description: Export a YouTube transcript as RAG chunks with deep links via VideoToText MCP. Use when the user wants vector-store chunks, embeddings input, or timestamped citations for AI retrieval.
---

# Export transcript for RAG

Use this skill when the user wants RAG chunks, embedding-ready segments, or deep-linked citations from a video.

## Steps

1. Ensure a transcript exists (`cliptext_get_transcript` if needed).
2. Call `cliptext_export_for_rag`.
3. Present:
   - Number of chunks
   - Example chunk with `deep_link` / timestamp
   - How to store chunks in a vector DB (id, text, metadata)
4. If the user also needs a raw export, call `cliptext_get_formats` with `json`, `md`, `srt`, `vtt`, `csv`, or `txt`.

## Rules

- Keep chunk text exactly as returned — do not rewrite before storage advice.
- Preserve deep links so citations jump back into the video.
- Mention API credits / plan limits if the tool reports them.
