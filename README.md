# 🔋 Solelot - מפת מיחזור סוללות בישראל

> **Find battery recycling points near you in Israel**

An interactive map showing **~3,900 battery recycling locations** across Israel — collection points at major retail chains and dedicated recycling facilities.

🌐 **[Live Site → zeevmala.github.io/solelot](https://zeevmala.github.io/solelot/)**

---

## Features

- **Interactive Map** — Browse all recycling points on a Leaflet.js map with marker clustering
- **Search** — Find locations by name, address, or city with autocomplete suggestions
- **Navigation** — Get directions via Google Maps or Waze directly from any point
- **Location Details** — View address, hours, and distance from your position
- **Multiple Basemaps** — Switch between street and light map styles
- **PWA** — Install as an app on your phone, works offline
- **Accessible** — Keyboard navigation, ARIA labels, screen reader support
- **Mobile Friendly** — Responsive design with bottom drawer sidebar on small screens

## Location Types

| Marker | Type | Examples |
|--------|------|----------|
| 🟢 | Collection Points | Superpharm, Shufersal, Home Center, Pelephone, Cellcom |
| 🔴 | Recycling Facilities | Batte-Re (Dimona), RE-CAR (Arad), MILI |

## Tech Stack

| | |
|---|---|
| **Frontend** | HTML, CSS, JavaScript (no frameworks) |
| **Maps** | [Leaflet.js](https://leafletjs.com/) + [MarkerCluster](https://github.com/Leaflet/Leaflet.markercluster) |
| **Tiles** | [CartoDB](https://carto.com/basemaps/) (Voyager & Positron) |
| **Hosting** | GitHub Pages |
| **PWA** | Service Worker + Web App Manifest |

## Project Structure

```
├── index.html        # Page structure (Hebrew, RTL)
├── style.css         # Styling and responsive layout
├── app.js            # Map logic, search, markers, sidebar
├── locations.json    # ~3,900 recycling locations
├── sw.js             # Service worker for offline/PWA
├── manifest.json     # PWA manifest
├── scraper.js        # Data collection script
└── icons/            # App icons (72px → 512px)
```

## Run Locally

No build tools needed — just open the files:

```bash
# Clone the repo
git clone https://github.com/Zeevmala/solelot.git
cd solelot

# Serve with any static server
npx serve .
# or
python -m http.server 8000
```

Then open `http://localhost:8000` (or whatever port your server uses).

## Data

Location data is stored in `locations.json` with this structure:

```json
{
  "locations": [
    {
      "id": 1,
      "name": "סופר פארם - דיזנגוף סנטר",
      "address": "דיזנגוף 50, תל אביב",
      "city": "תל אביב",
      "lat": 32.0753,
      "lng": 34.7748,
      "type": "store",
      "hours": "08:00-22:00",
      "description": ""
    }
  ]
}
```

## License

MIT
