# GPS Location Map 📡

A web application that visualizes GPS location data from NMEA sentences on an interactive map.

## Live Demo

🌐 [View the app here](https://nghiahieuhoang.github.io/gps-map-app)

## About

This project is part of the **IoT For Beginners** course assignment:  
**"Deploy your app"** — 3-Transport / Lesson 3: Visualize Location Data.

The app reads GPS coordinates parsed from NMEA sentences (generated via [nmeagen.org](https://nmeagen.org)) and displays them on an interactive map using **Leaflet.js** with OpenStreetMap tiles.

## Features

- 📍 Plots GPS coordinates on an interactive map
- 🛣️ Draws the route path between GPS frames
- 📊 Displays telemetry: speed, elevation, satellites, course
- 🖱️ Click any marker to see full frame details

## Tech Stack

| Tool | Purpose |
|------|---------|
| HTML / CSS / JavaScript | Frontend |
| [Leaflet.js](https://leafletjs.com/) | Interactive map rendering |
| [OpenStreetMap](https://www.openstreetmap.org/) | Map tiles (free, no API key required) |
| GitHub Pages | Hosting / Deployment |

## Note on API Keys

OpenStreetMap was chosen as the tile provider because it is free and requires no API key.  
If a provider requiring a subscription key (e.g. Azure Maps) were used, the key would be stored as an environment variable in Azure Static Web Apps — never hardcoded in the source.

## GPS Data Source

NMEA sentences were generated using [nmeagen.org](https://nmeagen.org) and parsed with a Python script (`read_nmea.py`) to extract:
- Date & Time (UTC)
- Speed (knots / km/h)
- Course (degrees)
- Elevation (meters)
- Number of satellites

## How to Run Locally

Just open `index.html` in any browser — no server or dependencies needed.
