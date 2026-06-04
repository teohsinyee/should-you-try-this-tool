# 2026-06-05 README Visitor-First Inventory Decision

## Status

Accepted

## What I Decided

### 1. Keep everything important in `README.md`

I want the value of this repo to be obvious from the main page.

### 2. Optimize the README for visitors, not maintainers

I do not want the README to explain itself too much. I want it to show the tools.

### 3. Keep the inventory as a table

A table is still the fastest way to scan multiple tools. Other layouts made media bigger, but slowed reading down.

### 4. Use a 4-column HTML table

I settled on these columns:
- `Tool`
- `Takeaway`
- `Verdict`
- `Media`

More columns made the layout wider, weaker, and less useful.

### 5. Prioritize column widths this way

I want the layout to roughly follow this split:
- `Tool` about 15%
- `Takeaway` about 25%
- `Verdict` about 10%
- `Media` about 50%

This matches how I want people to read it:
- media matters most visually
- takeaway matters more than tool width
- verdict should stay compact

### 6. Use GIF as the README preview format

GIF works better than MP4 inside README because people can see motion immediately.

I still want the full MP4 kept as a secondary link.

### 7. Use badge-style verdicts

Verdicts should be easy to scan. Badges are clearer than plain inline code.

Current color decisions:
- `Useful` = green
- `Promising` = blue
- `Niche` = gray
- `Skip` = red
- `Revisit` = yellow

### 8. Put GitHub links inside the tool cell

If the destination is a GitHub repo, the tool name should be clickable and `org/repo` can sit underneath.

I do not want a whole extra column just for links.

## Alternatives Considered

### Separate link column

Rejected because it wasted space and shrank the preview.

### Per-tool sections instead of a table

Rejected because it made scanning slower.

### Markdown table instead of HTML table

Rejected because GitHub gave me too little control over width.

### Full-width media row with `colspan`

Rejected because it looked awkward and broke the clean scan pattern.
