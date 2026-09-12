# ⚡ Hos Battery

**Windows power, battery health & wear telemetry utility — portable, offline, no telemetry.**

Hos Battery is a lightweight, single-executable Windows utility that gives you deep insight into your laptop's battery: real-time charge/discharge curves, saved multi-day history, wear analytics, longevity forecasts, smart power automation, and one-click backups — all computed locally on your machine. No cloud. No accounts. No background bloat.

> Built for Windows 10 / 11 (x64) · .NET 10 WPF · MVVM · 100% offline

---

## ✨ Features

### 🔋 Dashboard
- Live battery percentage, status, power source, time-remaining estimate
- Wear level, health %, design vs. full-charge capacity comparison
- Cycle count, voltage, chemistry and OEM info straight from WMI/ACPI
- Live status feed with alarms and system events
- **Desktop fallback** — clean AC-power mode when no battery is present

### 📈 Analytics & Interactive Curves
- **Interactive charge & discharge curve** of any saved day — pick a day, filter by `Both / Charge / Drain`
- **±%/h rate timeline** mini-chart (toggleable) — see exactly when your battery drained fastest
- **Sleep-gap aware plotting** — the curve breaks across sleep/off periods instead of faking drain
- Area fills, Y-axis (0–100%) gridlines, time axis, rich hover tooltips (time · % · state · rate)
- **Longevity Intelligence** — composite health score /100, wear-slope regression forecast ("≈ when you'll hit 80% health"), tracking age and estimated remaining lifespan
- **Curve CSV export** per selected day (timestamp, %, state, rate)
- Unique-named HTML battery reports (never overwrites; auto-opens in browser)

### 📜 History
- Chronological session archive: every AC plug-in/out with energy deltas (mWh)
- CSV / TXT export, one-click clear

### 📱 Live Tiles & Lock Screen
- Push battery telemetry to the Windows lock screen / widget surface

### ⚡ Power Plans & Automation
- One-click power plan switching, OEM plan listing via `powercfg`
- **Smart Power Automation** (offline, powercfg only):
  - Auto-switch plan on AC ↔ battery (High performance ↔ Balanced)
  - Force **power saver** below a configurable low-battery threshold
  - **Full-charge unplug reminder** when idle at 100% (gentle, 30-min cooldown)

### 🎯 Energy Drainers
- Real-time background-process CPU/memory monitor with energy impact badges
- One-click "End task" to stop battery killers

### 🎯 Calibration Assistant
- Guided 4-phase BMS recalibration checklist with progress tracking and best practices

### 🔋 Battery Types Encyclopedia
- All laptop chemistries (Li-ion, Li-Po, LiFePO₄, NiMH, NiCd, SLA, Solid-State) with full dossiers
- Pros / cons / care protocols, side-by-side comparison table, long-form educational guides

### 🔔 Alarms & Notifications
- Configurable low-battery (default 20%) and full-charge (default 80%) audio + visual alarms
- Looping audio alert option, test buttons, dismissible banner

### 💾 Data Safety
- **One-click ZIP backup** of all history/curves/settings → restore anytime
- All data stored locally in `%LocalAppData%\HosBattery` — nothing leaves your PC

### 🎨 Shell & UX
- Live tray icon rendering the actual battery % (32×32)
- Dark / Light / System theme (Windows 11 Fluent tokens, fully themeable)
- Borderless custom-window shell, multi-monitor aware
- **Single-instance guard** — launching twice focuses the running window
- Optional start-with-Windows, minimize-to-tray-on-close

---

## 📥 Download & Run

### Option 1 — Portable (recommended)
1. Grab `Hos Battery.exe` from the latest release.
2. Double-click. Done.

No installer, no admin rights, no registry changes. The app creates its data folder (`%LocalAppData%\HosBattery`) on first run.

> The portable build is **self-contained**: the .NET runtime is baked into the exe (~90 MB). Runs on a clean Windows 10/11 x64 machine with nothing installed.

### Option 2 — Framework-dependent build
Requires the [.NET 10 Desktop Runtime (x64)](https://dotnet.microsoft.com/download) installed; the exe is much smaller (~5 MB).

---

## 🗂️ Where does my data live?

```
%LocalAppData%\HosBattery\
├── charging_history.json      # session archive
├── battery_curve.json         # saved curve samples (all days)
├── settings.json              # alarms, theme, preferences
└── power_automation.json      # automation toggles
```

Backups go to `%UserProfile%\HosBattery Backups\` (zip).
CSV exports go to `%UserProfile%\HosBattery Exports\`.

---

## 🔒 Privacy

- **No network access. No telemetry. No analytics. No accounts.**
- Every byte stays on your disk. Delete the data folder → app is factory-fresh.

---

## 📄 License

© 2026 Hassan Ahmed. All rights reserved.

---

**Hos Battery** — *know your battery, extend its life.* 🔋
