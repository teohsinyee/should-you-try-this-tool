# 2026-06-05 README Visitor-First Inventory Spec

## Scope

This is the maintenance target I want future updates to follow.

## README Structure

I want `README.md` to stay simple:

1. Title
2. Hook sentence
3. One-line repo description
4. Inventory
5. Recently Added
6. Verdicts

Avoid adding extra sections unless they serve visitors directly.

## Inventory Format

Use an HTML table for the inventory.

Required columns:
- `Tool`
- `Takeaway`
- `Verdict`
- `Media`

Target width split:
- `Tool` about 15%
- `Takeaway` about 25%
- `Verdict` about 10%
- `Media` about 50%

## Tool Cell Rules

- The tool name should be clickable.
- If the link is a GitHub repo, prefer a GitHub URL on the tool name itself.
- Show `org/repo` as supporting text when useful.
- Keep this cell compact.

## Takeaway Rules

- Use one sentence only.
- Combine what the tool does with why it matters.
- Write for fast understanding, not completeness.

## Verdict Rules

- Use badge-style verdicts in the table.
- Keep verdict colors consistent with the current mapping.
- Keep the legend in the `Verdicts` section aligned with the table style.

## Media Rules

- If the source is video, create a short GIF for the README preview.
- Keep the original MP4 as a secondary link.
- Do not use raw MP4 as the main README preview.
- The media cell should show:
  - GIF preview
  - `Watch full video` link when MP4 exists

Recommended filenames:
- `assets/images/<tool-slug>.gif`
- `assets/images/<tool-slug>.png`
- `assets/videos/<tool-slug>.mp4`

## Agent Workflow

When I provide:
- a tool name
- a link
- a verdict or short opinion
- a screenshot path or video path

the agent should:
- prepare the assets
- convert video to GIF when appropriate
- update the README
- keep the verdict styling consistent
- preserve the current table layout

## Relationship to AGENTS.md

`AGENTS.md` is the operational rulebook for the AI agent.

This file records the current target so future updates can stay consistent without repeating the same debates.
