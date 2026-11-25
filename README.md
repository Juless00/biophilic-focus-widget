# Biophilic Focus — Notion Widget

A self-contained, embeddable HTML widget with a biophilic (nature-inspired) aesthetic. Designed for Notion `/embed`, but works anywhere you can iframe a public URL.

## What it includes
- **Live clock/date/greeting** with timezone support
- **Editable intention** — click the intention (or “Edit”) to set your own; saved in browser `localStorage`
- **3 daily habits** — check off habits; click a habit label to rename it; checks auto-reset each day (per timezone/date)
- **Pomodoro timer** — 25 min focus / 5 min break, Start/Pause/Reset, mode switch; state persisted in `localStorage`
- **Theme toggle** — cycles `auto/light/dark` (saved in `localStorage`)
- **Pomodoro sound** — optional chime on timer completion (click the bell icon to enable; browser requires a user gesture)
- **Daylight flow** — subtle progress bar showing how far through the day you are
- **Biophilic design** — sage/earth palette, organic leaf SVG, soft texture

## Embed in Notion
1. Host on a public HTTPS URL (GitHub Pages works).
2. In Notion, type `/embed` and paste the URL.
3. Resize to roughly **~760px wide × ~420px tall** for the full interactive layout.

## URL parameters
| Param | Example | Purpose |
|---|---|---|
| `name` | `?name=Jules` | Adds your name to the greeting |
| `focus` | `?focus=Finish%20the%203DB%20draft` | Sets initial intention (can be edited in-widget) |
| `theme` | `?theme=dark` | `auto` (default), `light`, or `dark` |
| `tz` | `?tz=Africa/Accra` | IANA timezone; defaults to browser timezone |

## Persistence / Notion caveat
Interactive state is saved in **browser `localStorage`** (key: `biophilic-focus-v1`). This works in normal browsers, but in Notion embeds some browsers/privacy settings may partition or block third-party iframe storage. If storage is blocked, the widget still works, but edits/timer/habit state may not persist across reloads. For reliable cross-device persistence, connect it to a small backend/Notion API proxy.

## Dev notes
- Single file, no build step, no external dependencies.
- Deploy by pushing `index.html` to the GitHub Pages repo.