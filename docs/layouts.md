# Dashboard layouts

R-Speedo has ten dashboard layouts. Layouts 1–5 are fixed cockpit styles; Layouts 6–10 are distinct workflows with their own job, data, and user expectation.

| Layout | Main job | What it emphasizes |
| --- | --- | --- |
| 1 | Tesla-style cockpit | Speed, battery, trip/ODO, range, electrical telemetry, location, and temperature |
| 2 | Sloped cockpit | Large speed gauge, RPM, gear, battery, power/current, temperatures, trip, and range |
| 3 | Gecit-style cockpit | Speed gauge, mini-map option, range, trip, configurable telemetry slots, and vehicle indicators |
| 4 | Tilano-style cockpit | Speed/RPM, drive mode, battery/power/current, attitude/inclinometer, and optional media player |
| 5 | Tech Lab | Switchable speed/incline/compass/level hero, sensor cards, motion calibration, and telemetry presets |
| 6 | Route/navigation | Map, destination search, route tools, energy/charging context, stations, workshops, and Cervo mirror |
| 7 | Motovlog | Camera recording, snapshots, gallery, intercom mic, telemetry sidecar/overlay, storage, remux, and sharing |
| 8 | Dragger | GPS acceleration timing, splits, readiness, personal best, ghost/rival, leaderboard, evidence, and race card |
| 9 | Road Dyno | Paired road pulls, readiness/cooldown, baseline/candidate, energy, sag, temperature, and tuning guidance |
| 10 | Custom Canvas | Up to five local dashboards with configurable telemetry/media/map/camera/image/text/icon widgets |

## Fixed cockpit layouts

### Layout 1 — Tesla-style cockpit

A balanced everyday dashboard with a large speed readout, battery/SOC, gear, ODO/trip, location, range, voltage, current, power, and motor/controller temperature.

### Layout 2 — Sloped cockpit

A speed-first sloped gauge with RPM and gear context, battery/SOC, voltage, power, current, motor/controller temperature, ODO, trip, range, and location.

### Layout 3 — Gecit-style cockpit

A round speed gauge with range, trip, clock, configurable telemetry rows, vehicle indicators, and an optional mini-map. Its telemetry slots can be selected from Settings.

### Layout 4 — Tilano-style cockpit

A cockpit focused on speed and RPM with drive-mode context, battery/SOC and voltage, power/current, motor/controller temperature, attitude/inclinometer data when motion access is available, and an optional media player.

### Layout 5 — Tech Lab

A sensor-focused layout where the hero instrument can switch between speed, incline, compass, and level. Sensor cards expose pitch/roll/heading state, motion calibration, location, and configurable telemetry presets.

## How to choose

- Want a clean everyday instrument panel? Choose Layout 1, 2, 3, or 4.
- Want sensors and configurable telemetry emphasis? Choose Layout 5 Tech Lab.
- Want navigation and charging decisions? Choose Layout 6.
- Want to vlog a ride? Choose Layout 7.
- Want acceleration timing and competition? Choose Layout 8 Dragger.
- Want to compare controller/setup changes? Choose Layout 9 Road Dyno.
- Want to build your own dashboard? Choose Layout 10 Canvas.

The fixed layouts share the same app telemetry state. Layout-specific settings should change presentation without silently changing the meaning or source of the underlying vehicle data.
