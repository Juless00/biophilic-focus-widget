# Biophilic Focus — Notion Widget

A self-contained, embeddable HTML widget with a biophilic (nature-inspired) aesthetic. Designed for Notion `/embed`, but works anywhere you can iframe a public URL.

## What it shows
- **Live clock** (HH:MM:SS) with timezone label
- **Date** and time-of-day greeting
- **Today's intention** — a daily rotating focus prompt, or your own custom text
- **Daylight flow** — a subtle progress bar showing how far through the day you are
- **Biophilic design** — sage/earth palette, organic leaf SVG, soft texture, auto light/dark

## Embed in Notion
1. Host the folder on a public HTTPS URL (GitHub Pages is the easiest).
2. In Notion, type `/embed`.
3. Paste the widget URL and resize the block.

## GitHub Pages quick setup
1. Create a GitHub repo and add `index.html` from this folder.
2. In repo settings, enable **Pages** from the `main` branch (root).
3. Your URL will look like: `https://<username>.github.io/<repo>/`

## URL parameters
Customize by adding query params:

| Param | Example | Purpose |
|---|---|---|
| `name` | `?name=Jules` | Adds your name to the greeting |
| `focus` | `?focus=Finish%20the%203DB%20draft` | Overrides the daily intention text |
| `theme` | `?theme=dark` | `auto` (default), `light`, or `dark` |
| `tz` | `?tz=Africa/Accra` | IANA timezone; defaults to browser timezone |

**Example:**
```
https://<username>.github.io/<repo>/?name=Jules&theme=auto&tz=Africa/Accra&focus=Build%20with%20calm%20focus
```

## Notes
- Single file, no build step, no external dependencies.
- Works best in Notion at ~700px wide and ~300px tall, but is responsive.
- Keep API keys/secrets out of widget files if you later add external data sources.
