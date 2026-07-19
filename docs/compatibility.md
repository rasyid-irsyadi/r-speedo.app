# R-Speedo compatibility

Last verified: 2026-07-19

This page describes integrations available in R-Speedo 1.0.29. "Integrated" means the application contains a maintained connection, parser, or UI path for that device family. It does not mean every model, firmware, clone, or third-party adapter has been physically verified.

## Motor controllers and vehicle telemetry

| Device or family | Type | Connection | Supported R-Speedo platforms | Status | Last verified | Known limitations |
| --- | --- | --- | --- | --- | --- | --- |
| Votol | Controller | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Compatibility and writable settings vary by controller, firmware, and adapter |
| Fardriver | Controller | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Compatibility and available telemetry vary by controller, firmware, and adapter |
| Gesits | Vehicle telemetry | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Read-only telemetry; available fields depend on the vehicle/device |
| Polytron profile with external ESP32 Votol CAN module | Vehicle telemetry module | BLE JSON advertised as `Votol_BLE` | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Experimental, unofficial | 2026-07-19 | Requires a separate unofficial module; controller-setting writes are unavailable |

## Battery management systems

| Device or family | Type | Connection | Supported R-Speedo platforms | Status | Last verified | Known limitations |
| --- | --- | --- | --- | --- | --- | --- |
| JK BMS | BMS | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Model, protocol, and firmware variants may expose different fields |
| Daly BMS | BMS | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Model, protocol, and firmware variants may expose different fields |
| ANT BMS | BMS | Bluetooth | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated | 2026-07-19 | Model, protocol, and firmware variants may expose different fields |

## Additional sensors

| Device or family | Type | Connection | Supported R-Speedo platforms | Status | Last verified | Known limitations |
| --- | --- | --- | --- | --- | --- | --- |
| BLE TPMS front/rear | Tire pressure sensor | BLE advertisement | Web/PWA with Web Bluetooth; Android APK native Bluetooth | Integrated where advertisement format is supported | 2026-07-19 | Pressure, temperature, battery, freshness, and warning fields depend on the advertisement format |

## Multi-battery

R-Speedo supports configuring multiple battery packs and pairing a BMS per pack. This is a runtime configuration and aggregation feature, not a guarantee that every pack combination is safe to combine.

The app distinguishes pack visibility, connected state, estimated state, active state, and aggregate values. Aggregation can be rejected or degraded when data is incomplete or unsafe to combine.

## Platform requirements

### Web/PWA

- A secure `https://` page.
- A browser and operating system with Web Bluetooth support for controller, BMS, or TPMS telemetry.
- User-granted Bluetooth and location permissions as required.
- The page may need to remain active because background execution is controlled by the browser and operating system.

GPS-only mode remains available when Web Bluetooth is unavailable.

### iPhone/iPad

- Safari iOS: Bluetooth telemetry is not available; GPS-only, route, report, and demo viewing can still work through normal web/location APIs.
- Bluefy or another WebBLE browser: experimental/user-tested workaround for BLE telemetry; UX and reliability depend on the third-party browser.
- There is no Android APK equivalent for iPhone.

### Android APK

- Android Bluetooth and location permissions as required by the device and Android version.
- An active R-Speedo APK entitlement and periodically refreshed offline license.
- Native integrations cover Bluetooth, background recording, file operations, start-on-boot, and the home-screen telemetry widget where available.
- Background behavior remains subject to Android settings, power management, and permissions.

## Before choosing hardware

Check the exact model, firmware, communication protocol, and Bluetooth adapter. A matching brand name alone is insufficient because manufacturers may change protocols between product revisions.

If a device is not listed, [open an issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues) with:

- Device brand and exact model.
- Firmware or hardware revision, if visible.
- Bluetooth device name.
- Whether the test used Web/PWA, Android APK, or an iPhone WebBLE workaround.
- A description of the connection result without personal data or credentials.

Do not post license tokens, account details, raw location history, credentials, or other sensitive data.
