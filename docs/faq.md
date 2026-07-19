# R-Speedo frequently asked questions

Last verified: 2026-07-19

## What is R-Speedo?

R-Speedo is a PWA and Android EV dashboard that uses phone GPS and, when available, Bluetooth telemetry from supported motor controllers, vehicle modules, BMS devices, and sensors.

## Does R-Speedo require Bluetooth?

No. GPS-only mode supports speed, route, distance, basic trip/report features, and GPS-based Dragger attempts. Bluetooth is required for controller, battery-cell, current, fault, tire-pressure, and other hardware telemetry.

## Does R-Speedo require internet access?

Some dashboard and locally stored trip features can continue without a live connection. Maps, route search, account/license refresh, live riders, charging-station/workshop updates, analytics upload, leaderboard sync, and other server-backed features require connectivity.

## Which controllers and BMS devices are supported?

R-Speedo includes integrations for Votol and Fardriver controllers, Gesits read-only telemetry, the independent Polytron ESP32 Votol CAN module path, JK BMS, Daly BMS, ANT BMS, and supported BLE TPMS formats. Exact compatibility depends on model, firmware, protocol, adapter, browser, and operating system. See [compatibility](compatibility.md).

## Does it work with Polytron motorcycles?

There is an experimental Polytron profile for an external ESP32 Votol CAN module that sends BLE JSON as `Votol_BLE`. It is independent of Polytron, and writing controller settings is unavailable.

## What is the difference between the PWA and Android APK?

The PWA runs from a browser and can be installed where browser support allows. Bluetooth requires Web Bluetooth support, and background execution is limited by the browser and operating system. The Android APK uses native Bluetooth, background recording, file handling, start-on-boot, account/offline-license integrations, and an Android telemetry widget.

## Does R-Speedo work on iPhone or iPad?

Safari can be used for GPS-only web features where location support is available, but Safari does not provide native Web Bluetooth telemetry. Bluefy or another WebBLE browser may work as an experimental user-tested workaround. There is no iPhone APK.

## What is Layout 8 Dragger?

Layout 8 Dragger is a GPS-based performance mode. It measures split times, compares against personal best or a rival ghost, syncs eligible runs to a leaderboard, and exposes public evidence without raw coordinates. It is not official race timing equipment. See [reports and data](reports-and-data.md).

## What is the Android telemetry widget?

The Android APK can update a home-screen widget with a compact ride, parked, charging, completed-charge, or last-status snapshot. It keeps a last-known-good view instead of replacing it with invalid data.

## How do charge sessions work?

When R-Speedo has enough battery/charging information, it can show an active or completed charge session with SOC, ETA, energy added, estimated cost, voltage, temperature, and cell-delta warnings. Accuracy depends on the telemetry source and configuration.

## Is the Android APK free?

APK access is managed through an R-Speedo account and purchase/activation status. Pricing and payment methods can vary, so use the current information shown in the app instead of relying on a copied price.

## What data does EV analytics collect?

EV analytics uses an anonymous app-device identifier with privacy guards and reduced location-derived metrics. Web/PWA and Android controls can differ, so review the current in-app consent text. Analytics is separate from optional live-rider location sharing. See [privacy](privacy.md).

## Can R-Speedo replace the vehicle's original instrument cluster?

Do not treat it as the only safety-critical instrument. Phones, GPS, Bluetooth, background execution, configuration, and third-party hardware can fail or drift. Follow manufacturer limits and local regulations.

## Why do speed, state of charge, range, or Dragger times differ from another display?

The displays may use different sensors, calibration values, sampling intervals, filters, capacity settings, start detection, or estimation models. See the [EV telemetry guide](ev-telemetry-guide.md).

## What should I do if my device is not listed?

Open a [GitHub issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues) with the exact model, revision, Bluetooth name, platform, and observed result. Do not include credentials, license tokens, raw traces, or location history.
