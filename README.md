<div align="center">

# 🛸 FlyNat — Pilot's Flight Nation

### End-to-end ecosystem for drone flight management, real-time airspace awareness, and regulatory compliance

[![Website](https://img.shields.io/badge/🌐_Website-flynat.net-2563eb?style=for-the-badge&logoColor=white)](https://flynat.net)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)]()

<br/>

FlyNat is a **2-platform aviation ecosystem** built for drone pilots, operators, and fleet managers.  
It combines a real-time UTM mobile app with professional telemetry analysis on desktop —  
giving pilots the tools they need in the field, and the data they need in the office.

### How the platforms connect

The two apps work together as a complete flight lifecycle system:

1. **Fly** — record your flight with any DJI, FPV, or Elios drone
2. **Import** — load the raw telemetry log into **FlyNat Desktop** (drag & drop)
3. **Sync** — the processed flight automatically appears in your **FlyNat Mobile** logbook
4. **Review** — view your GPS track, stats, and full technical breakdown on your phone — anywhere

> The Desktop app is the processing engine. Mobile is the field companion.  
> Logs must be imported into Desktop first before they appear in the mobile logbook.

</div>

---

## 📱 Tier 1 — FlyNat Mobile App

> Real-time UTM situational awareness, digital logbook, live pilot coordination, and weather — all in one field app.

<br/>

### 🗺️ Live Airspace Map & NOTAMs

FlyNat renders official airspace layers directly on the map in real time — updated from national AIP data. Every active NOTAM is pinned to its exact location. Tap any zone or marker to see full details: type, radius, altitude ceiling, valid time, and issuing authority.

<div align="center">
<table>
<tr>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/MobileNotamOnMap.jpeg" width="220" alt="NOTAMs on Live Map"/><br/>
  <sub><b>NOTAMs pinned on the live map</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/MobileNotamMsgs.jpeg" width="220" alt="NOTAM Messages Feed"/><br/>
  <sub><b>NOTAM message feed for active pilot</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/MobilenotamGNSSmsgs.jpeg" width="220" alt="GNSS Interference Alerts"/><br/>
  <sub><b>Real-time GNSS interference alerts</b></sub>
</td>
</tr>
</table>
</div>

**Airspace layers displayed:**

| Layer | Source | Description |
|---|---|---|
| 🔵 CTR Zones | eAIP Israel | Control zones around airports — tap for active frequencies |
| 🔴 Restricted (LLR/LLP/LLU) | eAIP Israel | No-fly and limited zones with full boundary data |
| 🟢 Nature Reserves (RATAG) | eAIP Israel | Protected natural areas — special permit required |
| 🟡 Active NOTAMs | Live feed | Temporary restrictions, events, military exercises |
| 🟠 GNSS Interference | Live feed | Active GPS jamming/spoofing zones broadcast in real time |

<br/>

### 🏛️ Official UTM Layers — Sourced from CAAI (RATA)

All airspace data is sourced directly from the **Israeli Civil Aviation Authority (RATA)** via the official eAIP publication. Layers are rendered with exact boundaries, altitudes, and operational details — identical to what official aeronautical charts show.

<div align="center">
<table>
<tr>
<td align="center" width="25%">
  <img src="https://flynat.net/assets/RataOfficialLayersUTM.jpeg" width="180" alt="Official UTM Layers"/><br/>
  <sub><b>All official layers on the map</b></sub>
</td>
<td align="center" width="25%">
  <img src="https://flynat.net/assets/RataCTRinfo.jpeg" width="180" alt="CTR Zone Info"/><br/>
  <sub><b>CTR — Control zone details</b></sub>
</td>
<td align="center" width="25%">
  <img src="https://flynat.net/assets/RataRestrictedInfo.jpeg" width="180" alt="Restricted Zone Info"/><br/>
  <sub><b>LLR/LLP/LLU — Restricted zones</b></sub>
</td>
<td align="center" width="25%">
  <img src="https://flynat.net/assets/RataNatureInfo.jpeg" width="180" alt="Nature Reserve Info"/><br/>
  <sub><b>RATAG — Nature reserves</b></sub>
</td>
</tr>
</table>
</div>

Tapping any zone opens a full detail panel: **zone name · type · altitude floor & ceiling · operating hours · responsible authority · permit requirements**.

<br/>

---

### 🛩️ Live Pilot Sharing & Pre-Flight Coordination

Any pilot who enables sharing appears on the map of nearby pilots in real time. Tap their marker to open a full pilot card: name, rank, drone model, current AGL altitude, mission type, and a direct WhatsApp link for immediate coordination.

Before a flight, pilots can perform a **Pre-Flight Check** with another pilot in the area — view their planned altitude, mission type, and send a direct message to coordinate separation.

<div align="center">
<table>
<tr>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/LivePilotOnmap.jpeg" width="220" alt="Live Pilot on Map"/><br/>
  <sub><b>Nearby pilots visible on the map in real time</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/MobileInfoPilotOnmap.jpeg" width="220" alt="Pilot Profile Card"/><br/>
  <sub><b>Tap a pilot marker to view their full profile</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/MobilePreflightcheckbetweenPilots.jpeg" width="220" alt="Pre-Flight Coordination"/><br/>
  <sub><b>Pre-flight coordination between two pilots</b></sub>
</td>
</tr>
</table>
</div>

- Each pilot shares: **drone model · altitude AGL · mission type · GPS position**
- Sharing is always **opt-in** — pilots choose when to appear on the map
- All shared data is **ephemeral** — disappears when the pilot stops sharing

<br/>

### 💬 Pilot-to-Pilot Chat

FlyNat includes a built-in encrypted messaging system between pilots — no WhatsApp, no phone number required. Start a conversation directly from the map by tapping another pilot's marker.

**How it works:**
- Tap any pilot on the live map → open their profile card → start a chat
- Messages are delivered instantly via **Firebase Realtime Database**
- **Push notifications** (FCM) alert pilots to new messages even when the app is in the background
- Each conversation shows the other pilot's **name, rank, drone model, and profile photo**
- Conversations can be cleared at any time — soft delete keeps history private without data loss

> Designed for quick pre-flight coordination, airspace deconfliction, and on-the-spot communication between pilots operating in the same area.

<br/>

---

### 🌤️ Weather Forecast — 24 Hours

Tap anywhere on the map to get a precise 24-hour hourly weather forecast for that exact GPS coordinate, powered by the Open-Meteo API. No need to switch apps — wind speed, gusts, cloud cover, precipitation probability, and visibility are shown inline.

<div align="center">
  <img src="https://flynat.net/assets/MobileWeather24hrs.jpeg" width="280" alt="24-Hour Weather Forecast"/>
  <br/><sub><b>24-hour hourly forecast — tap any point on the map</b></sub>
</div>

<br/>

**Weather data includes:**
- 🌬️ Wind speed & gust (m/s) — critical for flight safety decisions
- ☁️ Cloud cover (%) and cloud base altitude
- 🌧️ Precipitation probability per hour
- 👁️ Visibility distance
- 🌡️ Temperature and humidity

<br/>

---

### 📖 Digital Logbook & Flight Records

Every flight recorded via FlyNat Mobile is automatically saved to the pilot's digital logbook. Each entry includes the full GPS track rendered on an interactive map, alongside all technical data from the session.

<div align="center">
<table>
<tr>
<td align="center" width="50%">
  <img src="https://flynat.net/assets/MobileLogBook.jpeg" width="260" alt="Mobile Logbook List"/><br/>
  <sub><b>Full logbook — filterable by date, drone, or mission type</b></sub>
</td>
<td align="center" width="50%">
  <img src="https://flynat.net/assets/MobileFlightInfo.jpeg" width="260" alt="Flight Info and Track"/><br/>
  <sub><b>Flight details with GPS track rendered on map</b></sub>
</td>
</tr>
</table>
</div>

**Each logbook entry records:**

| Field | Details |
|---|---|
| 📅 Date & Time | Start and end timestamp |
| ⏱️ Duration | Total airtime in HH:MM:SS |
| 📍 GPS Track | Full route rendered on interactive map |
| 📐 Max Altitude | Peak AGL altitude reached |
| 🚀 Max Speed | Maximum ground speed recorded |
| 🛸 Drone Model | Platform used for the flight |
| 🎯 Mission Type | Survey / Inspection / Photography / Training / Other |
| 📝 Free Note | Custom pilot annotation (e.g. "Roof scan, client X, engineer approval") |

<br/>

---

### 📡 Live Session History

Every flight performed with location sharing active is automatically saved to the pilot's session history. The record is structured for instant display to a field inspector — no paperwork, no delay.

<div align="center">
  <img src="https://flynat.net/assets/MobileSessionHistory.jpeg" width="280" alt="Live Session History"/>
  <br/><sub><b>Session history — complete record of every shared flight</b></sub>
</div>

<br/>

Each session record includes: **start/end time · duration · max altitude · max speed · GPS coordinates · drone model · mission type · pilot note**

<br/>

---

### 📊 Statistics, Ranks & Achievements

FlyNat tracks every pilot's cumulative flight activity and awards ranks, badges, and achievements automatically from the logbook — no manual input required.

<div align="center">
  <img src="https://flynat.net/assets/MobilePilotStats.jpeg" width="280" alt="Pilot Statistics"/>
  <br/><sub><b>Pilot statistics — ranks, badges, and annual flight summary</b></sub>
</div>

<br/>

---

## 🖥️ Tier 2 — FlyNat Desktop Analytics

> Professional telemetry analysis, deep diagnostics, and fleet logbook management for operators and companies.

FlyNat Desktop ingests raw telemetry files from multiple drone platforms and transforms them into structured, readable aviation data. Built for serious operators, flight schools, and fleet managers who need more than basic CSV exports.

<div align="center">
<table>
<tr>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/FlynatDesktop.png" width="280" alt="FlyNat Desktop Main View"/><br/>
  <sub><b>Main logbook view — full fleet history</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/FlyNatStatsDesktop.png" width="280" alt="Statistics and Graphs"/><br/>
  <sub><b>Visual statistics — flight hours, trends, and metrics</b></sub>
</td>
<td align="center" width="33%">
  <img src="https://flynat.net/assets/FlyNatAdvancedStatsDesktop.png" width="280" alt="Advanced Analytics"/><br/>
  <sub><b>Advanced analytics — detailed breakdown by drone and pilot</b></sub>
</td>
</tr>
</table>
</div>

<br/>

### Supported Telemetry Formats

| Format | Source | Details |
|---|---|---|
| `.txt` (DJI) | DJI Go / DJI Fly | Full telemetry — battery, GPS, altitude, IMU, RC signal |
| `.bbl` / `.bfl` | FPV Blackbox | Raw Betaflight/Cleanflight logs decoded frame-by-frame |
| `.kml` / `.gpx` | Any GPS logger | Track import with timestamps and altitude |
| `.csv` | DJI / Generic / Drone Harmony | Structured data import with auto column mapping |
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

Generate official **PDF logbooks** and **CSV exports** containing full flight records — ready for:
- ✅ Civil aviation authority audits
- ✅ Insurance documentation
- ✅ Maintenance review records
- ✅ Fleet management reporting

### Sync with FlyNat Mobile

Once a flight log is imported and processed in Desktop, it is automatically pushed to the pilot's **FlyNat Mobile** logbook. The pilot can then view the full flight — GPS track, altitude profile, stats, and notes — directly from their phone, without carrying a laptop to the field.

<br/>

---

## 🔗 Links

| | |
|---|---|
| 🌐 Official Website | [flynat.net](https://flynat.net) |

---

<div align="center">
  <sub>Built for drone pilots · © 2026 FlyNat Solutions · <a href="https://flynat.net">flynat.net</a></sub>
</div>
