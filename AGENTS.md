# AGENTS.md

## Purpose

This repository is a visitor-first, README-first inventory of productivity tools.

The human owner is not expected to maintain files manually. In most cases, the human will only provide:
- a tool name
- a source link
- a short opinion or verdict
- a screenshot path, video path, or both

The agent is responsible for everything else.

## Source of Truth

- `README.md` is the only visitor-facing source of truth.
- Visitors should not need to open folders to understand the collection.
- Do not create per-tool markdown files or deep content hierarchies unless explicitly requested.

## Agent Responsibilities

When the user provides a new exploration, the agent should:
- copy or move media into the repo using stable filenames
- convert video into a short README-friendly GIF preview when appropriate
- keep the full video as a secondary asset when available
- update the inventory row in `README.md`
- update `Recently Added`
- update `Quick Stats`
- keep wording concise, scannable, and visitor-friendly
- prefer a specific link label such as `org/repo` for GitHub repositories

If the tool already exists in the inventory:
- update the existing row instead of creating a duplicate row
- refresh media and wording only when the new material is better or more current

## README Rules

- `README.md` must stay visitor-first.
- Put the most useful information near the top.
- Hide maintainer-oriented details from visitors unless explicitly requested.
- Keep each tool entry short and easy to scan.
- Treat the repo as an inventory, not a long-form review blog.

The inventory information should remain stable unless the user explicitly requests a redesign. By default, keep:
- `Tool`
- `Takeaway`
- `Verdict`
- `Media`
- `Link`

For this repository, the preferred inventory presentation is a 4-column HTML table in `README.md`:
- `Tool`
- `Takeaway`
- `Verdict`
- `Media`

Current layout priority:
- `Media` is the most visually important column and should stay large
- `Takeaway` is more important than `Tool`
- `Tool` should stay relatively narrow
- `Verdict` should stay compact

Current width target:
- `Tool` about 15%
- `Takeaway` about 25%
- `Verdict` about 10%
- `Media` about 50%

Do not switch away from the table layout unless the user explicitly asks.
Do not expand back to extra columns such as separate `What it does`, `Why it matters`, or `Link` unless the user explicitly asks.
For GitHub links, keep the clickable tool name in the `Tool` column and show `org/repo` as supporting text when useful.

## Media Rules

- Prefer GIF as the primary motion preview inside `README.md`.
- Do not use raw MP4 as the primary README preview.
- If the user provides a video, create a short GIF preview when the content is suitable.
- Keep the full MP4 as a secondary link such as `Watch full video`.
- Static screenshots are acceptable when a GIF is unnecessary or unavailable.
- Media should help visitors understand the tool quickly, not force them to watch a long demo.
- In the inventory table, prioritize readable media size over extra text detail.

Recommended file naming:
- `assets/images/<tool-slug>.gif`
- `assets/images/<tool-slug>.png`
- `assets/videos/<tool-slug>.mp4`

## Writing Style

- Write in clear, natural English unless the user asks otherwise.
- Optimize for fast understanding.
- The tone should feel like a quick, informed recommendation, not a technical manual.
- Avoid bloated explanations in the main inventory.

## Link Rules

- For GitHub repositories, use `org/repo` as the visible link label.
- For official websites, use the product or company name.
- Avoid generic labels like `GitHub`, `Website`, or `Link` when a more specific label is available.

## Verdict Display Rules

- Prefer badge-style verdicts in the inventory table instead of plain inline code when the user wants stronger visual scanning.
- Keep `Useful` green.
- If additional verdict colors are introduced later, keep them visually distinct and easy to scan.

## Commit Rules

Every commit must:
- use `codex@openai.com` as the git email
- follow Conventional Commits

Use commit messages that clearly separate content additions from repo or presentation changes.

### Content commits

Use `feat:` when adding or materially updating a tool entry, media preview, or other user-facing inventory content.

Examples:
- `feat: add microsoft intelligent terminal exploration`
- `feat: add gif preview for arc browser entry`
- `feat: refresh notion calendar verdict and demo`

### Infra or structure commits

Use these when changing repo scaffolding, presentation structure, or agent workflow rather than the inventory content itself:
- `feat:` for new repo capabilities or major structural additions
- `refactor:` for reorganizing structure without changing meaning
- `docs:` for agent instructions or non-visitor documentation updates
- `style:` for presentation-only README cleanup with no content change
- `chore:` for housekeeping that does not affect visitor-facing content

Examples:
- `feat: scaffold visitor-first productivity inventory`
- `docs: add agent workflow and commit guidance`
- `style: simplify readme layout for faster scanning`
- `refactor: reorganize asset naming conventions`
- `chore: normalize gitignore entries`

When in doubt:
- if the change adds or updates a tool exploration, treat it as content
- if the change updates repo rules, layout, naming, or workflow, treat it as infra/structure

## Default Workflow

When the user says something like:
- "video is here"
- "here is the link"
- "my verdict is this"

the agent should assume the user wants end-to-end handling:
- prepare assets
- generate GIF if needed
- update `README.md`
- keep the repo consistent
- choose the correct Conventional Commit category if a commit is requested
