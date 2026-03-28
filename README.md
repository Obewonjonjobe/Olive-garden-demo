# 🌿 Olive St. Community Garden — Solar Map & Planner

Interactive solar mapping, shadow analysis, and crop planning tools for the **Olive St. Community Garden** in Oxford, Michigan (42.82°N, 83.26°W · USDA Zone 5b–6a).

## Tools

### Solar Map (`/`)

Interactive visualization of sun exposure and tree shadow patterns across the garden throughout the year.

- **Live Mode** — Real-time sun position, shadow projection, and day/night visualization
- **Day Mode** — Full-day sun-hours heatmap showing cumulative light exposure per garden cell
- **Plant Mode** — Crop overlay on the sun heatmap with planting timeline, toggle individual crops on/off

Controls: time of day, week of year, tree height, tree distance from garden edge.

### Planting Guide (`/planting-guide`)

Sortable reference table for all 21 community-selected crops with planting timing, soil requirements, sun needs, and companion planting guilds.

## Garden Specs

| | |
|---|---|
| **Location** | 915 Olive Street, Oxford MI |
| **Coordinates** | 42°48'38"N 83°15'29"W |
| **Plot size** | ~110 ft (E–W) × 40 ft (N–S) |
| **Tree line** | South edge, ~50 ft mature hardwoods |
| **Zone** | USDA 5b–6a, last frost ~May 10–15 |

## Deploy to Vercel

### Option 1: GitHub + Vercel (recommended)

1. Push this repo to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/olive-st-garden.git
   git branch -M main
   git push -u origin main
   ```

2. Go to [vercel.com](https://vercel.com) and sign in with GitHub

3. Click **"Add New Project"** → Import your `olive-st-garden` repo

4. Vercel auto-detects the config. Click **Deploy**.

5. Your site will be live at `olive-st-garden.vercel.app` (or a custom domain)

### Option 2: Vercel CLI

```bash
npm i -g vercel
vercel
```

Follow the prompts. Vercel reads `vercel.json` and deploys the `public/` folder.

## Local Development

```bash
npx serve public
```

Opens at `http://localhost:3000`.

## Tech

Pure HTML/CSS/JS — no build step, no frameworks, no dependencies. Solar position math uses the standard astronomical equation of time and declination formula. Shadow projection uses trigonometric projection of tree height onto the garden plane accounting for solar azimuth.

## License

MIT
