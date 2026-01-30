# AI Prompts & Notes

Purpose
- Central, version-controlled store for reusable prompts, prompt templates, evaluations, and notes for various personal projects and utilities.

Quick start
1. Create a new repo (recommended: private) named `ai-prompts`.
2. Copy the files from this scaffold into the repository root.
3. Commit and push:
   - git add .
   - git commit -m "Initial scaffold for prompts repository"
   - git push origin main
4. Add repo-specific CONTRIBUTING.md and LICENSE if needed.

Structure
- prompts/: Prompt files and templates (organized by project).
  - templates/: canonical templates and examples.
  - <project-name>/: prompts grouped by project.
- notes/: Architecture and design notes (add if needed).
- experiments/: Short-lived experiment logs and artifacts (add if needed).
- assets/: Binary assets or datasets (use Git LFS for large files).
- .github/workflows/: Optional automation (evaluations, linting).

Conventions
- File names: `YYYY-MM-DD-short-slug-vN.md` (keeps chronological order).
- Use YAML frontmatter for structured metadata (title, date, project, model, version, tags, status).
- Versioning: bump `version` in frontmatter for meaningful prompt changes (v1, v2, ...).
- Sensitive data: Never commit API keys or secrets. Use GitHub Secrets or an external vault.

Searching & Indexing
- Use consistent tag names in frontmatter (project, intent, model).
- Optionally maintain `prompts/index.yml` or the `prompts/templates/README.md` as an index for important prompts.

Governance
- Add CONTRIBUTING.md to enforce frontmatter and structure for collaborators.
- Use PRs for changes to canonical prompts.
- Use Issues for experiments and tracking evaluation work.

Contact
- Repository owner: bmcgaugh