# R-Speedo

R-Speedo is a PWA and Android dashboard that turns a phone into an EV instrument panel using GPS and optional Bluetooth telemetry from supported motor controllers and battery management systems.

[Open R-Speedo](https://r-speedo.app/) · Last verified: 2026-07-19 · Current app version: 1.0.29

## What R-Speedo does

- Shows speed, battery, controller, trip, navigation, and charging-session information across eight dashboard layouts.
- Reads supported Votol, Fardriver, Gesits, and Polytron telemetry through an independent ESP32 Votol CAN module.
- Reads supported JK, Daly, and ANT battery management systems over Bluetooth.
- Supports BLE TPMS sensors for front/rear pressure, temperature, battery/freshness, and warnings when available.
- Works in GPS-only mode when no compatible Bluetooth hardware is available.
- Provides route planning, charging-station and workshop context, trip reports, exportable ride data, and optional live-rider sharing.
- Supports multiple configured battery packs with per-pack visibility and guarded aggregate telemetry.
- Includes Layout 7 for motovlog recording/snapshots and Layout 8 Dragger for GPS-based performance timing, evidence, ghost/rival runs, and leaderboards.
- Runs as a web/PWA app and as an Android APK with native Bluetooth, background recording, file handling, offline licensing, start-on-boot, and a home-screen telemetry widget.

## Screenshots and demo

Screenshots and video in this repository, when present, use synthetic demo data and public demo locations. Do not use private trips, real accounts, home locations, payment screens, admin screens, or raw recordings as public media.

The intended media set is:

- `media/hero-demo.mp4`
- `media/dashboard-landscape-dark.webp`
- `media/dashboard-portrait-light.webp`
- `media/route-demo.webp`
- `media/report-demo.webp`
- `media/layout-contact-sheet.webp`

## Supported integrations

| Category | Integration | Status |
| --- | --- | --- |
| Motor controller | Votol | Integrated |
| Motor controller | Fardriver | Integrated |
| Vehicle telemetry | Gesits | Integrated, read-only telemetry |
| Vehicle profile | Polytron with an external ESP32 Votol CAN module | Experimental and unofficial |
| BMS | JK | Integrated |
| BMS | Daly | Integrated |
| BMS | ANT | Integrated |
| Sensor | BLE TPMS front/rear | Integrated where advertisement format is supported |

An integrated brand or protocol is not a guarantee that every model, firmware version, clone, or third-party Bluetooth adapter will work. See the [compatibility notes](docs/compatibility.md) before choosing hardware.

## Important limitations

- Web/PWA Bluetooth requires a browser and operating system that implement Web Bluetooth.
- Safari on iPhone/iPad does not provide native Web Bluetooth support; GPS-only use still works where normal web/location APIs work.
- Bluefy or other WebBLE browsers on iPhone are user-tested workarounds, not the same as native iOS support.
- GPS-only mode cannot provide controller, cell, fault, current, or other hardware telemetry.
- Layout 8 Dragger is a GPS/performance mode with evidence and quality gates; it is not official race timing equipment.
- Mobile operating systems may suspend browser activity in the background; the Android APK provides additional native background support.
- Charging-station and workshop community data can be incomplete or outdated.
- Polytron integration requires an external unofficial module and does not support writing controller settings.
- R-Speedo is a monitoring aid, not a replacement for manufacturer limits, calibrated instruments, or safe riding practices.

## Documentation

- [Product overview](docs/product.md)
- [Hardware and platform compatibility](docs/compatibility.md)
- [Frequently asked questions](docs/faq.md)
- [Reports and data](docs/reports-and-data.md)
- [Privacy notes](docs/privacy.md)
- [EV telemetry guide](docs/ev-telemetry-guide.md)

## Ringkasan Bahasa Indonesia

R-Speedo adalah dashboard PWA dan Android yang mengubah ponsel menjadi panel instrumen kendaraan listrik. Aplikasi dapat memakai GPS saja atau membaca telemetri Bluetooth dari controller Votol/Fardriver/Gesits, BMS JK/Daly/ANT, TPMS BLE, dan modul Polytron ESP32 Votol CAN yang tidak resmi. R-Speedo juga memiliki peta/rute, sesi charging, report perjalanan, multi-battery, Layout 7 motovlog, Layout 8 Dragger, live rider, analytics anonim, APK premium, dan widget Android.

Dukungan perangkat tetap bergantung pada model, firmware, adapter, browser, sistem operasi, dan hasil verifikasi nyata. Harga dan metode pembayaran mengikuti flow resmi di aplikasi agar tidak basi.

## Official project

- Website: [r-speedo.app](https://r-speedo.app/)
- Maintainer: [Rasyid Irsyadi](https://github.com/rasyid-irsyadi)
- Corrections: [open an issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues)

R-Speedo is an independent project. References to vehicle, controller, BMS, browser, and platform brands do not imply affiliation or endorsement.

## License and trademarks

Original documentation in this repository is licensed under [Creative Commons Attribution 4.0 International](LICENSE).

The R-Speedo name and logo, third-party trademarks, manufacturer documentation, and third-party media are excluded from that license unless explicitly stated otherwise.
