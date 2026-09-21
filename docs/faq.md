# R-Speedo frequently asked questions

Last verified: 2026-09-21

## What is R-Speedo?

R-Speedo is a PWA and Android EV dashboard that uses phone GPS and, when available, Bluetooth telemetry from supported motor controllers, vehicle modules, BMS devices, and sensors.

## Does R-Speedo require Bluetooth?

GPS-only mode supports speed, route, distance, basic trip/report features, and GPS-based Dragger attempts. Compatible Bluetooth hardware adds controller, battery-cell, current, fault, tire-pressure, and other telemetry.

## Does R-Speedo require internet access?

Some dashboard and locally stored trip features can continue without a live connection. Maps, route search, account/license refresh, live riders, charging-station/workshop updates, analytics upload, leaderboard sync, and other server-backed features require connectivity.

## Which controllers and BMS devices are supported?

R-Speedo includes integrations for Votol and Fardriver controllers, read-only VESC controller telemetry, Gesits read-only telemetry, the independent Polytron ESP32 Votol CAN module path, JK/Daly/ANT/JBD BMS devices, supported BLE TPMS formats, and Cervo clock/navigation mirroring. Exact compatibility depends on model, firmware, protocol, adapter, browser, and operating system. See [compatibility](compatibility.md).

## Does it work with Polytron motorcycles?

There is an experimental Polytron profile for an external ESP32 Votol CAN module that sends BLE JSON as `Votol_BLE`. It is independent of Polytron, and writing controller settings is unavailable.

## Can R-Speedo tune a controller?

For supported protocols, yes. Votol exposes controller setting pages and Fardriver exposes confirmed writable fields with safety warnings and guards. VESC, Gesits, Polytron, and SFOX350 paths provide read-only or diagnostic telemetry where stated.

## What does multi-battery support mean?

You can pair a BMS per pack, keep pack visibility, see connected/estimated/active state, and use guarded aggregate telemetry. Incomplete or incompatible pack data keeps the display at per-pack or degraded aggregate state.

## What is the difference between the PWA and Android APK?

The PWA runs from a browser and can be installed where browser support allows. Bluetooth requires Web Bluetooth support, and background execution is limited by the browser and operating system. The Android APK uses native Bluetooth, background recording, file handling, start-on-boot, account/offline-license integrations, and an Android telemetry widget.

## Does R-Speedo work on iPhone or iPad?

Safari supports GPS-only web features where location support is available. Bluefy or another WebBLE browser provides an experimental Bluetooth path, and a native iOS test/sideload target exists. Android is the public premium native path.

## What is Layout 8 Dragger?

Layout 8 Dragger is a GPS-based performance mode. It measures split times, compares against personal best or a rival ghost, syncs eligible runs to a leaderboard, and exposes public evidence with coordinate-reduced route context. It provides practical rider comparison timing. See [reports and data](reports-and-data.md).

## What is Layout 7 Motovlog?

Layout 7 is a riding-vlog workflow: camera recording, pause/resume, snapshots, gallery, Bluetooth intercom mic, telemetry sidecar/overlay, native/web storage, and sharing. Android can remux supported MP4 recordings without re-encoding; browser and iOS behavior depends on platform storage and media limits.

## What is Layout 9 road Dyno?

Layout 9 compares paired local road pulls and can analyze time, energy, voltage sag, temperature, and minimum wheel-power/torque estimates when enough data is available. Readiness, cooldown, road, wind, slope, vehicle configuration, GNSS, and telemetry quality affect the road-based estimate.

## What is Layout 10 custom Canvas?

Layout 10 lets users arrange telemetry, media, map, camera, image, text, and icon widgets on up to five local portrait or landscape canvases. Canvas configuration can be exported or imported as JSON; locally selected image assets remain local unless the user exports or shares them.

## What is Hall of Fame?

Hall of Fame is an opt-in monthly public board for distance, elevation, and efficiency. New eligible foreground rides can contribute after joining, while personal reports remain available if synchronization fails. The board focuses on public performance summaries with coordinate-reduced route context.

## What does Cervo support do?

For a supported Alva Cervo BL-CERVO head unit, R-Speedo synchronizes time and mirrors Layout 6 navigation. Cervo fills the head-unit/navigation role.

## Where is the hardware Shop available?

The R-Speedo hardware Shop is available only in Indonesia. Current products, availability, IDR prices, and the WhatsApp handoff are shown by the app, so copied listings may become outdated.

## What is the Android telemetry widget?

The Android APK can update a home-screen widget with a compact ride, parked, charging, completed-charge, or last-status snapshot. It keeps a last-known-good view instead of replacing it with invalid data.

## How do charge sessions work?

When R-Speedo has enough battery/charging information, it can show an active or completed charge session with SOC, ETA, energy added, estimated cost, voltage, temperature, and cell-delta warnings. Accuracy depends on the telemetry source and configuration.

## Is the Android APK free?

APK access is managed through an R-Speedo account and purchase/activation status. Pricing and payment methods can vary, so use the current information shown in the app instead of relying on a copied price.

## What data does EV analytics collect?

EV analytics uses an anonymous app identifier, privacy filtering, and reduced location-derived metrics. Web/PWA and Android controls can differ, so review the current in-app consent text. Analytics is separate from optional live-rider location sharing. See [privacy](privacy.md).

## Can R-Speedo replace the vehicle's original instrument cluster?

Use it alongside safety-critical instruments. Phones, GPS, Bluetooth, background execution, configuration, and third-party hardware can fail or drift. Follow manufacturer limits and local regulations.

## Why do speed, state of charge, range, or Dragger times differ from another display?

Different sensors, calibration values, sampling intervals, filters, capacity settings, start detection, or estimation models can produce different values. See the [EV telemetry guide](ev-telemetry-guide.md).

## What should I do if my device is unlisted?

Open a [GitHub issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues) with the exact model, revision, Bluetooth name, platform, and observed result. Keep the report limited to device and connection details.
