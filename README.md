<div align="center">

# 🛸 FlyNat — Pilot's Flight Nation

### Digital logbook, flight diagnostics, and live pilot coordination for drone pilots

[![GitHub Release](https://img.shields.io/github/v/release/FlyNat/FlyNat?style=for-the-badge&label=Latest+Release&color=2563eb)](https://github.com/FlyNat/FlyNat/releases/latest)
[![Status](https://img.shields.io/badge/Server-Closed%20·%20Apps%20Live-orange?style=for-the-badge)]()

<br/>

> **ℹ️ Notice:** The FlyNat website and API server have been shut down.  
> The apps are **fully functional** and continue to be available here on GitHub.  
> Firebase-based features (live map, pilot chat, real-time sharing) remain active.  
> Features that required the API server (UAS NOTAM, DJI Pilot 2 Cloud) are no longer available.

<br/>

## ⬇️ Download

| App | Platform | Link |
|---|---|---|
| 📱 **FlyNat LogBook Mobile** | Android 8.0+ | [Download APK →](https://github.com/FlyNat/FlyNat/releases/latest) |
| 🖥️ **FlyNat LogBook Desktop** | Windows 10/11 | [Download EXE →](https://github.com/FlyNat/FlyNat/releases/latest) |

> Desktop app is **portable** — no installation required. Just run the `.exe`.

<br/>

---

## How the platforms connect

1. **Fly** — record your flight with any DJI, FPV, or Elios drone
2. **Import** — load the raw telemetry log into **FlyNat Desktop** (drag & drop) — or import directly on **Mobile**
3. **Review** — view your GPS track, stats, and full technical breakdown anywhere

<br/>

---

## 📱 FlyNat Mobile App

> Real-time pilot coordination, digital logbook, live map, and weather — all in one field app.

<br/>

### 🗺️ Live Map & Pilot Sharing

Any pilot who enables sharing appears on the map in real time. Tap their marker to open a full pilot card: name, drone model, current AGL altitude, mission type, and a direct contact link.

- Each pilot shares: **drone model · altitude AGL · mission type · GPS position**
- Sharing is always **opt-in**
- All shared data is **ephemeral** — disappears when the pilot stops sharing
- Powered by **Firebase** — no API server required

<br/>

### 💬 Pilot-to-Pilot Chat

Built-in messaging between pilots — no phone number required. Start a conversation directly from the map by tapping another pilot's marker.

- Messages delivered instantly via **Firebase Realtime Database**
- **Push notifications** (FCM) for new messages in background
- Each conversation shows the other pilot's name, drone model, and profile photo

<br/>

### 🌤️ Weather Forecast — 24 Hours

Tap anywhere on the map to get a precise 24-hour hourly weather forecast for that exact GPS coordinate, powered by Open-Meteo API.

**Weather data includes:** wind speed & gusts · cloud cover · precipitation probability · visibility · temperature

<br/>

### 📖 Digital Logbook & Log Import

Import DJI flight logs directly on Android — no desktop required. The logbook stores your full flight history with GPS tracks, battery data, and statistics.

**Supported import formats (Mobile):**
- DJI binary `.txt` logs (DJI Go / DJI Fly)
- CSV exports (AirData, Litchi)

<br/>

### 📊 Statistics, Ranks & Achievements

FlyNat tracks cumulative flight activity and awards ranks and badges automatically from the logbook.

<br/>

---

## 🖥️ FlyNat Desktop Analytics

> Professional telemetry analysis, deep diagnostics, and fleet logbook management for Windows.

FlyNat Desktop ingests raw telemetry files from multiple drone platforms and transforms them into structured aviation data.

<br/>

### Supported Telemetry Formats

| Format | Source | Details |
|---|---|---|
| `.txt` (DJI) | DJI Go / DJI Fly | Full telemetry — battery, GPS, altitude, IMU, RC signal |
| `.bbl` / `.bfl` | FPV Blackbox | Raw Betaflight/Cleanflight logs decoded frame-by-frame |
| `.kml` / `.gpx` | Any GPS logger | Track import with timestamps and altitude |
| `.csv` | DJI / AirData / Litchi / Drone Harmony | Structured data import with auto column mapping |
| `.json` (Elios) | Flyability Elios | Inspection drone logs parsed and visualized |

<br/>

### Analysis & Diagnostics

- **Battery curves** — voltage sag, cell delta, discharge rate across the full flight
- **GPS signal quality** — satellite count, HDOP, fix type per second
- **RC signal graph** — RSSI/link quality over time with dropout markers
- **Compass & IMU** — heading error spikes, vibration levels, error flags
- **Motor telemetry** — RPM, ESC temperature, motor imbalance detection
- **Anomaly detection** — automatic flagging of error events and out-of-range values

<br/>

### Regulatory Export

Generate official **PDF logbooks** and **CSV exports** ready for:
- ✅ Civil aviation authority audits
- ✅ Insurance documentation
- ✅ Maintenance review records
- ✅ Fleet management reporting

<br/>

---

## What's available vs. what's not

| Feature | Status |
|---|---|
| 📱 Mobile log import (DJI binary + CSV) | ✅ Available |
| 🖥️ Desktop log import & analysis | ✅ Available |
| 🗺️ Live pilot map (Firebase) | ✅ Available |
| 💬 Pilot-to-pilot chat (Firebase) | ✅ Available |
| 🌤️ Weather forecast | ✅ Available |
| 📊 Statistics & logbook | ✅ Available |
| 📄 PDF export | ✅ Available |
| 🚫 UAS NOTAM overlay | ❌ Server closed |
| 🚫 DJI Pilot 2 Cloud API | ❌ Server closed |

<br/>

---

<div align="center">
  <sub>Built for drone pilots · © 2026 FlyNat · <a href="https://github.com/FlyNat/FlyNat">github.com/FlyNat/FlyNat</a></sub>
</div>
