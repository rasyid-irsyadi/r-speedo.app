# R-Speedo product overview

Last verified: 2026-08-15

R-Speedo is a phone-based EV dashboard for riders who want one interface for speed, battery, controller, route, charging, performance, motovlog, and trip information. It can run with GPS only or combine GPS with telemetry from supported Bluetooth hardware.

## Intended users

- Riders who want a phone-based speedometer, range view, route panel, and trip report.
- EV builders and tuners who need live controller/BMS telemetry and diagnostics.
- Riders with multiple battery packs who need per-pack and guarded aggregate views.
- Android users who want native Bluetooth behavior, background recording, offline licensing, start-on-boot, private APK releases, and a home-screen telemetry widget.
- Riders who want Layout 7 motovlog recording, Layout 8 GPS-based Dragger timing, Layout 9 road Dyno analysis, or a custom Layout 10 Canvas.

## Operating modes

### GPS-only

GPS-only mode provides speed, route, distance, trip timing, basic reports, map views, and Dragger attempts without pairing a controller or BMS. It does not provide battery-cell data, controller faults, electrical current, BMS alarms, or other hardware telemetry.

### Bluetooth telemetry

R-Speedo can pair with supported motor controllers, BMS devices, TPMS sensors, or a combination of them. Available fields depend on the connected device, firmware, adapter, permissions, signal quality, and selected profile.

### Multiple battery packs

Users can configure multiple battery packs and pair a BMS per pack. R-Speedo can show pack visibility, connected/estimated state, warnings, and aggregate telemetry when the data is safe enough to combine.

## Main capabilities

- Ten dashboard layouts, including Tech Lab sensors, map/navigation, motovlog, Dragger, road Dyno, and a custom Canvas.
- Speed, trip, odometer, battery, controller, tire pressure, and fault monitoring when data is available.
- Route search, destination links, distance, ETA, charging-station and workshop context, and optional live-rider sharing.
- Charge session panel with ETA, energy, cost, voltage, temperature, and cell-delta warnings.
- Trip history, maps, charts, stop/charging/fault logs, data quality indicators, and exports.
- Layout 7 motovlog camera preview, recording controls, snapshots, gallery, and telemetry sidecar.
- Layout 8 Dragger GPS timing with readiness gate, split times, personal best, ghost/rival, leaderboard, public evidence, and report flow.
- Layout 9 local road Dyno with readiness/cooldown, paired two-way pulls, energy and voltage-sag analysis, minimum wheel-power/torque estimates when data is sufficient, and baseline/candidate comparison. It is not a chassis dynamometer.
- Layout 10 custom Canvas with up to five portrait or landscape canvases, configurable telemetry/media/map/camera/image/text/icon widgets, local backgrounds, and optional JSON import/export.
- An Indonesia-only hardware Shop with product availability, IDR pricing shown by the current app data, and WhatsApp handoff.
- Read-only VESC controller and JBD BMS telemetry, plus time synchronization and Layout 6 navigation mirroring for supported Alva Cervo BL-CERVO head units.
- Optional privacy-aware EV analytics for aggregate product and market-fit signals.
- Vehicle profiles, including multiple saved motorcycles and manufacturer profiles from the app data.

Feature availability can differ between Web/PWA and Android APK installations.

Layout 7 and Layout 8 assets may require an authenticated R-Speedo session.

## Web/PWA and Android APK

| Capability | Web/PWA | Android APK |
| --- | --- | --- |
| GPS-only dashboard | Available when browser location access is granted | Available when Android location access is granted |
| Bluetooth telemetry | Requires Web Bluetooth support | Uses native Android Bluetooth |
| Installation | Browser installation when PWA support is available | APK installation |
| Background trip support | Limited by browser and operating-system lifecycle rules | Additional native background recording support |
| Motovlog/media files | Browser storage/download behavior | Native file integration where available |
| Android widget | Not available | Home-screen telemetry widget |
| Account and license | Web dashboard features can be used without an APK license | APK access is managed through an R-Speedo account and offline license |

APK access, purchase methods, and availability may vary by country or account. This repository intentionally does not publish a static price.

## iPhone and iPad position

Safari on iPhone/iPad can be used for normal web features such as GPS-only dashboard use, route/report/demo viewing, and account pages where supported. Safari does not provide native Web Bluetooth support for BLE telemetry.

Bluefy or another WebBLE browser may work as a user-tested workaround for Bluetooth telemetry on iPhone. Treat this as experimental and more complicated than Android native Bluetooth.

R-Speedo also has a native iOS test/sideload target, but it is not a public release channel. Android remains the publicly distributed premium native app.

## Data and privacy

- Local dashboard and trip/report data are separate from anonymous analytics.
- Web/PWA analytics policy is shown in the app; Android APK provides analytics controls.
- Analytics uses an anonymous app-device identifier and privacy guards rather than a public rider profile.
- Sensitive telemetry is sanitized and vendor/export data is aggregated.
- Live-rider sharing is separate, optional, and location-based.
- A deletion-request flow exists for submitted analytics data.

Users should review the current in-app consent text before enabling analytics or live sharing because product behavior and regional requirements can change.

## Known limitations

- A software integration cannot guarantee compatibility with every hardware or firmware variant.
- Bluetooth availability, permissions, and background behavior differ by browser and operating system.
- GPS speed, distance, elevation, and Dragger timing are estimates affected by sensors, sampling, reception, filtering, and mounting.
- Battery state of charge and range estimates depend on correct vehicle configuration and source telemetry.
- Charging-station and workshop information may be incomplete or outdated.
- Layout 8 Dragger is a GPS/performance mode, not official timing equipment.
- Layout 9 road Dyno is affected by GNSS quality, road, wind, slope, mass/configuration, sampling, and source telemetry; its estimates are not chassis-dyno measurements.
- The hardware Shop is available only for Indonesia and its current product status remains authoritative in the app.
- The Polytron integration is unofficial, requires an external ESP32 Votol CAN module, and is monitoring-only for controller settings.

See [compatibility](compatibility.md), [reports and data](reports-and-data.md), [privacy](privacy.md), [frequently asked questions](faq.md), and the [EV telemetry guide](ev-telemetry-guide.md) for details.
