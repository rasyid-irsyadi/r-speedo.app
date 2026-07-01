# R-Speedo frequently asked questions

Last verified: 2026-07-01

## What is R-Speedo?

R-Speedo is a PWA and Android EV dashboard that uses phone GPS and, when available, Bluetooth telemetry from supported motor controllers and BMS devices.

## Does R-Speedo require Bluetooth?

No. GPS-only mode supports speed, route, distance, and basic trip/report features. Bluetooth is required for controller, battery-cell, current, fault, and other hardware telemetry.

## Does R-Speedo require internet access?

Some dashboard and locally stored trip features can continue without a live connection. Maps, route search, account/license refresh, live riders, charging-station updates, analytics upload, and other server-backed features require connectivity.

## Which controllers and BMS devices are supported?

R-Speedo includes integrations for Votol and Fardriver controllers and JK, Daly, and ANT BMS families. Exact compatibility depends on model, firmware, protocol, and adapter. See [compatibility](compatibility.md).

## Does it work with Polytron motorcycles?

There is an experimental, unofficial Polytron profile for an external ESP32 Votol CAN module that sends BLE JSON as `Votol_BLE`. It is not an official Polytron integration, and writing controller settings is unavailable.

## What is the difference between the PWA and Android APK?

The PWA runs from a browser and can be installed where browser support allows. Bluetooth requires Web Bluetooth support, and background execution is limited by the browser and operating system. The Android APK uses native Bluetooth, background recording, file, account, and offline-license integrations.

## Does R-Speedo work on iPhone or iPad?

The web interface and GPS-only features depend on the browser's normal web and location support. Bluetooth telemetry requires Web Bluetooth support, which is not available in every browser or operating system. Check the current browser capability before relying on BLE.

## Is the Android APK free?

APK access is managed through an R-Speedo account and purchase/activation status. Pricing and payment methods can vary, so use the current information shown in the app instead of relying on a copied price.

## What data does EV analytics collect?

EV analytics is opt-in and uses an anonymous app-device identifier with privacy guards and reduced location-derived metrics. It is separate from optional live-rider location sharing. Review the current in-app consent screen before enabling either feature.

## Can R-Speedo replace the vehicle's original instrument cluster?

Do not treat it as the only safety-critical instrument. Phones, GPS, Bluetooth, background execution, configuration, and third-party hardware can fail or drift. Follow manufacturer limits and local regulations.

## Why do speed, state of charge, or range differ from another display?

The displays may use different sensors, calibration values, sampling intervals, filters, capacity settings, or estimation models. See the [EV telemetry guide](ev-telemetry-guide.md).

## What should I do if my device is not listed?

Open a [GitHub issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues) with the exact model, revision, Bluetooth name, platform, and observed result. Do not include credentials, license tokens, or location history.
