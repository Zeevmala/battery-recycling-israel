# Battery Recycling Map - Specification

## Requirements
- Display interactive map of Israel
- Show battery recycling locations with markers
- Click markers to see location details (name, address, hours)
- Mobile-friendly design
- Hebrew language support (RTL)

## Tech Stack
- **HTML** - Page structure
- **CSS** - Styling and responsive layout
- **JavaScript** - Interactivity and map logic
- **Leaflet.js** - Open-source map library (free, no API key needed)
- **OpenStreetMap** - Map tiles

## Milestones

### M1: Basic Map with Dummy Data ✅
- [x] Set up project files (index.html, style.css, app.js)
- [x] Display map centered on Israel
- [x] Add 3-5 test markers with popups
- [x] Basic styling

### M2: Real Location Data ✅
- [x] Create locations data file (JSON)
- [x] Add all store locations (Superpharm, Shufersal, etc.)
- [x] Add recycling facilities (Batte-Re, RE-CAR, MILI)
- [x] Different marker icons by location type
- [x] Location details in popups

### M3: Search & Filters ✅
- [x] Filter by location type (stores vs facilities)
- [x] Search by city/area
- [x] "Find nearest" using user location
- [x] Mobile-responsive controls
