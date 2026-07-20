# Salt Spring Trip Costs — Project Notes

## What this is
A single-page website showing the cost breakdown for a Salt Spring Island /
North Saanich long-weekend trip (Aug 21–23, 2026), styled as a paper receipt.
Made to share with the 7 people on the trip.

## Who it's for
Samantha (owner, edits it herself) and her trip group (viewers).

## Tech
- One file: `index.html` — all styles and code live inside it, no build step
- Font: Geist Mono, loaded from Google Fonts
- Chart: Chart.js (stacked bar), loaded from a CDN
- Hosted on GitHub Pages from the `main` branch

## Constraints & standing rules
- Keep it a single self-contained `index.html` — easy to tweak by hand
- Any cost changes must update three places: the chart data, the stat tiles,
  and the line items (plus grand total / per-person). Flag if they drift.
- Follow the global CLAUDE.md rules (git save points, plain-English summaries)
