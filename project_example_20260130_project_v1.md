---
title: "Search assistant: extract and summarize relevant passages"
date: 2026-01-30
author: "bmcgaugh"
project: "project-example"
version: "v1"
status: "active"
model: "gpt-4o"
temperature: 0.0
tokens_limit: 1200
tags:
  - "search"
  - "summarization"
  - "excerpt"
source: ""
---

## Intent
Given a user query and a set of candidate passages, rank passages by relevance and return a concise summary + a short excerpt for the top 3.

## Prompt (canonical)
System: You are an assistant that ranks and summarizes passages for information retrieval. Be factual and concise.

User: Given the user query and the candidate passages, return:
1) A ranked list of the top 3 passages (by id) with a 1-line justification each.
2) For each top passage, a concise 2–3 sentence summary of why it answers the query.
3) For each top passage, include a short excerpt (single sentence) copied verbatim from the passage that supports the summary.
Output must be valid JSON with fields: query, results (array of objects with id, score, justification, summary, excerpt).

Do not fabricate passage contents. If none are relevant, return results: [] and a brief explanation.

## Input example
{
  "query": "How do I rotate images in Python using Pillow?",
  "passages": [
    {"id": "p1", "text": "Using PIL.Image.rotate you can rotate images by degrees..."},
    {"id": "p2", "text": "To crop an image with Pillow use image.crop(box)..."},
    {"id": "p3", "text": "Pillow supports rotate and transpose operations; rotate(angle, expand=True)..."}
  ]
}

## Expected output (example)
{
  "query": "How do I rotate images in Python using Pillow?",
  "results": [
    {
      "id": "p3",
      "score": 0.95,
      "justification": "Explains rotate syntax and expand option.",
      "summary": "Pillow's rotate(angle, expand=True) rotates an image by the specified degrees and can expand the canvas to fit rotated content.",
      "excerpt": "Pillow supports rotate and transpose operations; rotate(angle, expand=True)..."
    },
    ...
  ]
}

## Success criteria
- JSON parseable by a strict JSON parser.
- Top results are truly relevant and justifications align with passages.

## Notes
- Use low temperature to improve determinism.
- Ensure outputs are traceable to passages (no hallucinated excerpts).