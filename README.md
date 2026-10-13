# Uptown Tonight

Every deal Uptown, by the clock. A phone-first site for Miami students planning a night in Oxford, OH: which bars they can get into, what each one is running, and when.

## What's here

| File | What it is |
| --- | --- |
| `index.html` | The whole app: age switch, 7-day strip, deals grouped by time of night, detail sheet. No build step. |
| `deals.json` | The data: bar profiles, deals, closures. The app loads it on start. |
| `brand/` | Brand kit tokens and guidelines (colors, type, bar line colors, voice). |
| `netlify.toml` | Netlify config: serves the repo root as a static site. |

## Rules the data follows

- **Fall 2026 sources only** (Aug 15, 2026 onward). Older info is dropped, not kept as "maybe".
- **Every drink special is 21+ with a valid ID.** Bars marked 18+ let 18 to 20 year olds in with X's on their hands. The 18 to 20 view leads with covers, food and events and tucks drink specials into a 21+ section.
- Every deal records its `source` and the date it was `seen`. Missing prices are `null` with status `needs_price`, never guessed.

## Updating deals

Edit `deals.json` and push. Each deal looks like:

```json
{ "id": "skippers-thu", "bar": "skippers", "type": "drink", "title": "Liquor Pitcher Night",
  "days": ["thu"], "date": null, "start": null, "end": null, "all_day": false,
  "price": "$9 liquor pitchers", "steps": [], "status": "confirmed",
  "source": "bar_ig_post", "seen": "2026-10-02", "notes": null }
```

- `type`: `drink`, `clock`, `cover`, `food`, `event`
- `days` for weekly deals, or `date` (YYYY-MM-DD) for a one-night thing
- `start` / `end` in 24h `HH:MM`; `steps` for clocks whose price changes over the night
- `status`: `confirmed`, `needs_price`, `verify`, `one_off`
- Rentals go in `closures`: `{ "date": "2026-10-17", "bar": "brick-street", "status": "confirmed", "note": "" }`

## Deploying

Netlify, connected to this repo, publish directory `.`, no build command. Every push to `main` goes live. Custom domain: a `joeykoski.com` subdomain.

## Later

The plan is a VPS with a real database (bars, deals, closures, crowd reports for rentals and lines). `deals.json` is already shaped like those tables, so it imports directly.
