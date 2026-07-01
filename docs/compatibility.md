# R-Speedo compatibility

Last verified: 2026-07-01

This page describes integrations available in R-Speedo 1.0.10. “Integrated” means the application contains a maintained connection and parser for that device family. It does not mean every model, firmware, clone, or third-party adapter has been physically verified.

## Motor controllers

| Integration | Connection | Web/PWA | Android APK | Status | Limitations |
| --- | --- | --- | --- | --- | --- |
| Votol | Bluetooth | Requires Web Bluetooth | Native Bluetooth | Integrated | Compatibility and writable settings vary by controller, firmware, and adapter |
| Fardriver | Bluetooth | Requires Web Bluetooth | Native Bluetooth | Integrated | Compatibility and available telemetry vary by controller, firmware, and adapter |
| Polytron profile with external ESP32 Votol CAN module | BLE JSON advertised as `Votol_BLE` | Requires Web Bluetooth | Native Bluetooth | Experimental, unofficial | Requires a separate unofficial module; controller-setting writes are unavailable |

## Battery management systems

| Integration | Connection | Web/PWA | Android APK | Status | Limitations |
| --- | --- | --- | --- | --- | --- |
| JK BMS | Bluetooth | Requires Web Bluetooth | Native Bluetooth | Integrated | Model, protocol, and firmware variants may expose different fields |
| Daly BMS | Bluetooth | Requires Web Bluetooth | Native Bluetooth | Integrated | Model, protocol, and firmware variants may expose different fields |
| ANT BMS | Bluetooth | Requires Web Bluetooth | Native Bluetooth | Integrated | Model, protocol, and firmware variants may expose different fields |

R-Speedo supports configuring multiple battery packs and pairing a BMS per pack. Aggregated values are only as reliable as the data supplied by each connected BMS and the pack configuration entered by the user.

## Platform requirements

### Web/PWA

- A secure `https://` page.
- A browser and operating system with Web Bluetooth support for controller or BMS telemetry.
- User-granted Bluetooth and location permissions as required.
- The page may need to remain active because background execution is controlled by the browser and operating system.

GPS-only mode remains available when Web Bluetooth is unavailable.

### Android APK

- Android Bluetooth and location permissions as required by the device and Android version.
- An active R-Speedo APK entitlement and periodically refreshed offline license.
- Background behavior remains subject to Android settings, power management, and permissions.

## Before choosing hardware

Check the exact model, firmware, communication protocol, and Bluetooth adapter. A matching brand name alone is insufficient because manufacturers may change protocols between product revisions.

If a device is not listed, [open an issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues) with:

- Device brand and exact model.
- Firmware or hardware revision, if visible.
- Bluetooth device name.
- Whether the test used Web/PWA or Android APK.
- A description of the connection result without personal data or secrets.

Do not post license tokens, account details, private keys, raw location history, or other sensitive data.
