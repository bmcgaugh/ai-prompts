# Prompt templates

This folder contains canonical prompt templates and guidance for adding new prompts.

Recommended workflow to add a prompt:
1. Copy `prompt-template.md` and fill the frontmatter and sections.
2. Save as `YYYY-MM-DD-short-slug-v1.md` under `prompts/<project-name>/`.
3. Open a PR if collaborating — reviewers should check intent, success criteria, and safety considerations.

Frontmatter fields (required/recommended)
- title: Short descriptive title
- date: YYYY-MM-DD
- author: Name or handle
- project: project-name
- version: v1, v2 ...
- status: draft | active | deprecated
- model: intended model (e.g., gpt-4o)
- temperature: numeric
- tokens_limit: integer (optional)
- tags: list of strings
- source: link or reference (optional)

Keep prompts small, explicit, and include examples + expected outputs for testing.