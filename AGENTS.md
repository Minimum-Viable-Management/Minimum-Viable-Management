# Repository Guidance for Agents

## Structure

- Keep all topic notes under `topics/` with filenames matching the linked titles (kebab-case).
- Root directory holds `README.md`, `AGENTS.md`, original transcripts/PDFs/etc. (left uncommitted and unreferenced), and no additional markdown guides.

## README Expectations

- Each bullet must retain its emoji-prefixed link label and one-sentence description.
- Maintain the `## 🎧 Listen & Subscribe` section with the four podcast links and the `## 📺 Episode Guide` section linking to new YouTube episode URLs.
- End with the call-to-action paragraph inviting issues/PRs.

## Topic Pages

- File names and H1 titles must stay in sync with the README labels and emojis (e.g. `# 🗣️ Minimum Viable One-on-Ones`).
- Section headings use emoji prefixes:
  - `## 🔑 Key Points`
  - `## 🛠️ Put It Into Practice`
  - `## 🎧 Episode Reference`
  - `## 🔗 Related Resources` (optional, include when needed)
  - `## 📌 Highlights to Explore` (only for the reading list page)
- Reference external sources with canonical URLs (LeadDev, mikemcquaid.com, YouTube playlist).
- Episode references must link to the playlist URLs with timestamp notes in parentheses when available.

## Formatting Conventions

- One sentence per line across all Markdown files; preserve existing blank-line spacing.
- Use Markdown lists for key points and practice steps; continuation sentences should align under the list marker.
- Keep text ASCII where possible; emoji already in use should remain unchanged.
- Insert blank lines around headings and before/after lists so `markdownlint` stays clean.
- Prefer British English spellings (e.g. “organisation”) and avoid abbreviations by spelling words out fully.
- Write “e.g.” and “i.e.” without trailing commas to satisfy Vale rules.

## Linking Rules

- Do not reference or commit local `.txt` or `.pdf` files inside content; always link to public URLs instead.
- Ensure README bullets link to `topics/*.md` paths, not root-level files.
- Maintain the podcast links: YouTube playlist, Apple Podcasts, Spotify, Riverside RSS.

## Tooling

- Install markdown linters with `brew install vale markdownlint-cli`.
- Run `markdownlint .` and `vale .` before submitting changes to keep prose and formatting consistent.

## General Notes

- When adding new topics, mirror the established pattern: create the `topics/` file with matching emoji/title, update the relevant themed list in `README.md`, and keep descriptions to a single sentence.
- Summaries should focus on actionable guidance drawn from transcripts, LeadDev articles, or Mike’s posts.
- Respect the existing emoji taxonomy; introduce new emojis only if the theme clearly differs and stays consistent between README and topic page.
