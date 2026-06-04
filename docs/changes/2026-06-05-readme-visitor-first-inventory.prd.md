# 2026-06-05 README Visitor-First Inventory

## Goal

I want this repo to help people decide quickly whether a new productivity tool is worth trying.

I want everything important to be visible from `README.md`.

I do not want visitors to open folders just to understand the tool.

I also do not want to maintain files manually.

In practice, I only want to provide:
- a tool name
- a link
- a short verdict or opinion
- a screenshot path, video path, or both

I want the AI agent to handle everything else.

## Visitor Needs

When someone lands here, I believe they mainly care about:
- what the tool is
- whether it is worth trying
- the quick verdict
- a visual preview
- where to click next

They do not need my internal maintenance logic in the main README.

## Requirements

- `README.md` must be the main visitor-facing surface.
- Inventory content must stay easy to scan.
- Media must be large enough to matter visually.
- The inventory should remain table-based for quick scanning.
- GitHub links should be obvious and specific.
- Verdicts should be visually easy to recognize.
- Video should not be shown as raw MP4 inside the README.
- The repo should include agent instructions so AI can maintain the format consistently.

## Why AGENTS.md Exists

I created `AGENTS.md` so AI can maintain this repo without turning me into the file editor.

It exists to preserve:
- README structure
- inventory rules
- media rules
- verdict presentation
- commit conventions
