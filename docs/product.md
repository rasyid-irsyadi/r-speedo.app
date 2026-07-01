# R-Speedo product overview

Last verified: 2026-07-01

R-Speedo is a phone-based EV dashboard for riders who want one interface for speed, battery, controller, route, and trip information. It can run with GPS only or combine GPS with telemetry from supported Bluetooth hardware.

## Operating modes

### GPS-only

GPS-only mode provides speed, route, distance, and basic trip/report features without pairing a controller or BMS. It does not provide battery-cell data, controller faults, electrical current, or other hardware telemetry.

### Bluetooth telemetry

R-Speedo can pair with supported motor controllers, BMS devices, or both. Available fields depend on the connected device, firmware, adapter, permissions, and signal quality.

### Multiple battery packs

Users can configure multiple battery packs and pair a BMS per pack. R-Speedo can aggregate available pack telemetry for dashboard, warning, and reporting views. Hardware combinations still need model-level verification.

## Main capabilities

- Six instrument-panel layouts.
- Speed, trip, odometer, battery, controller, and fault monitoring when data is available.
- Route search, destination links, distance, and ETA.
- Trip history, maps, charts, stop/charging/fault logs, and report export.
- Charging-station discovery, bookmarks, suggestions, and reports.
- Optional nearby live-rider sharing.
- Optional privacy-aware EV analytics.
- Vehicle profiles, including multiple saved motorcycles.

Feature availability can differ between web/PWA and Android APK installations.

## Web/PWA and Android APK

| Capability | Web/PWA | Android APK |
| --- | --- | --- |
| GPS-only dashboard | Available when browser location access is granted | Available when Android location access is granted |
| Bluetooth telemetry | Requires Web Bluetooth support | Uses native Android Bluetooth |
| Installation | Browser installation when PWA support is available | APK installation |
| Background trip support | Limited by browser and operating-system lifecycle rules | Additional native background recording support |
| File operations | Browser download/import behavior | Native file integration where available |
| Account and license | Web features can be used without an APK license | APK access is managed through an R-Speedo account and offline license |

APK access, purchase methods, and availability may vary by country or account. This repository intentionally does not publish a fixed price.

## Data and privacy

- EV analytics is opt-in.
- Analytics uses an anonymous app-device identifier rather than a rider profile for telemetry ingestion.
- Sensitive telemetry is sanitized and location-derived metrics are reduced before analytics submission.
- Events can be queued offline and sent later after consent.
- A deletion-request flow is available for submitted analytics data.
- Live-rider sharing is a separate optional feature and requires location permission.

Users should review the current in-app consent text before enabling analytics or live sharing because product behavior and regional requirements can change.

## Known limitations

- A software integration cannot guarantee compatibility with every hardware or firmware variant.
- Bluetooth availability, permissions, and background behavior differ by browser and operating system.
- GPS speed, distance, and elevation are estimates affected by device sensors, sampling, reception, and filtering.
- Battery state of charge and range estimates depend on correct vehicle configuration and source telemetry.
- Charging-station and community-contributed information may be incomplete.
- The Polytron integration is unofficial, requires an external ESP32 Votol CAN module, and is monitoring-only for controller settings.

See [compatibility](compatibility.md), [frequently asked questions](faq.md), and the [EV telemetry guide](ev-telemetry-guide.md) for details.
