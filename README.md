# GeoScan Pro — Location Intelligence Dashboard

A fully advanced, professional location intelligence dashboard using IP + GPS data. Zero dependencies except Bootstrap CDN and Google Fonts.

## Features

- **Multi-API IP fallback chain** — tries ipwho.is → ip-api.com → freeipapi.com → ipinfo.io automatically
- **Exact GPS location** — 7 decimal precision, accuracy bar, altitude, speed, heading
- **Reverse geocoding** — full address, mohalla, district, postcode via Nominatim
- **Dark-filtered OpenStreetMap** embed with coordinate HUD
- **IP vs GPS comparison** — Haversine distance, city/country match analysis
- **Network info** — download speed, RTT, connection type
- **Device fingerprint** — browser, OS, GPU, CPU cores, RAM, battery, touch
- **Export** — JSON download, CSV download, copy all to clipboard
- **Scan history** — last 5 scans stored in session
- **Toast notifications** — live feedback on every step
- **Progress bar** — visual scan progress

## IP APIs Used (automatic fallback)

| API | Free | CORS | Rate Limit |
|-----|------|------|------------|
| ipwho.is | ✅ | ✅ | 10k/month |
| ip-api.com | ✅ | ✅ | 45 req/min |
| freeipapi.com | ✅ | ✅ | 60 req/min |
| ipinfo.io | ✅ | ✅ | 50k/month |

## Usage

Just open `index.html` in a browser. No build step needed.

For best GPS accuracy, use on a device with GPS hardware (phone/laptop with location hardware) and click "Allow" when browser asks for location permission.

> **Note:** IP location only works when hosted (HTTP/HTTPS). For local `file://` testing, IP APIs may be blocked by CORS — use a local server like `npx serve .` or just deploy to GitHub Pages.

## Deploy to GitHub Pages

1. Fork / clone this repo
2. Go to Settings → Pages
3. Set source to `main` branch, `/ (root)`
4. Your dashboard will be live at `https://yourusername.github.io/repo-name`

## Accuracy Guide

| GPS Accuracy | Level |
|---|---|
| ≤ 5 m | Exact ghar / door number |
| ≤ 15 m | Gali / street level |
| ≤ 40 m | Mohalla level |
| ≤ 100 m | Area level |
| > 100 m | Weak GPS signal |

## Tech Stack

- HTML5 / CSS3 / Vanilla JavaScript
- Bootstrap 5.3
- JetBrains Mono + Outfit (Google Fonts)
- OpenStreetMap + Nominatim (reverse geocoding)
- Browser Geolocation API
- Network Information API
- Battery Status API
- WebGL (GPU detection)

## License

MIT
