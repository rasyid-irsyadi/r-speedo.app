# R-Speedo

R-Speedo is a PWA and Android dashboard that turns a phone into an EV instrument panel using GPS and optional Bluetooth telemetry from supported motor controllers and battery management systems.

[Open R-Speedo](https://r-speedo.app/) · Last verified: 2026-08-15 · Current app version: 1.0.47

## What R-Speedo does

- Shows speed, battery, controller, trip, navigation, and charging-session information across ten dashboard layouts.
- Reads supported Votol, Fardriver, and VESC controller telemetry, plus Gesits and an experimental unofficial Polytron module path.
- Reads supported JK, Daly, ANT, and JBD battery management systems over Bluetooth.
- Can synchronize time and mirror Layout 6 navigation to a supported Alva Cervo BL-CERVO head unit.
- Supports BLE TPMS sensors for front/rear pressure, temperature, battery/freshness, and warnings when available.
- Works in GPS-only mode when no compatible Bluetooth hardware is available.
- Provides route planning, charging-station and workshop context, trip reports, exportable ride data, and optional live-rider sharing.
- Supports multiple configured battery packs with per-pack visibility and guarded aggregate telemetry.
- Includes Layout 7 for motovlog recording/snapshots and Layout 8 Dragger for GPS-based performance timing, evidence, ghost/rival runs, and leaderboards.
- Includes Layout 9 road Dyno for local paired-pull analysis and Layout 10 Canvas for custom telemetry dashboards.
- Provides an Indonesia-only hardware Shop with product details and WhatsApp handoff.
- Runs as a web/PWA app and as an Android APK with native Bluetooth, background recording, file handling, offline licensing, start-on-boot, and a home-screen telemetry widget.

## Screenshots and demo

Public screenshots and video are planned but are not published yet. When added, they will use synthetic demo data and safe public locations.

## Supported integrations

| Category | Integration | Status |
| --- | --- | --- |
| Motor controller | Votol | Integrated |
| Motor controller | Fardriver | Integrated |
| Motor controller | VESC | Integrated, read-only telemetry |
| Vehicle telemetry | Gesits | Integrated, read-only telemetry |
| Vehicle profile | Polytron with an external ESP32 Votol CAN module | Experimental and unofficial |
| Head unit | Alva Cervo BL-CERVO | Time synchronization and navigation mirroring |
| BMS | JK | Integrated |
| BMS | Daly | Integrated |
| BMS | ANT | Integrated |
| BMS | JBD | Integrated, read-only telemetry |
| Sensor | BLE TPMS front/rear | Integrated where advertisement format is supported |

An integrated brand or protocol is not a guarantee that every model, firmware version, clone, or third-party Bluetooth adapter will work. See the [compatibility notes](docs/compatibility.md) before choosing hardware.

## Important limitations

- Web/PWA Bluetooth requires a browser and operating system that implement Web Bluetooth.
- Safari on iPhone/iPad does not provide native Web Bluetooth support; GPS-only use still works where normal web/location APIs work.
- Bluefy or other WebBLE browsers on iPhone are user-tested workarounds, not the same as native iOS support.
- A native iOS test/sideload target exists, but there is no public native iOS release.
- GPS-only mode cannot provide controller, cell, fault, current, or other hardware telemetry.
- Layout 8 Dragger is a GPS/performance mode with evidence and quality gates; it is not official race timing equipment.
- Layout 9 road Dyno produces practical estimates from road and telemetry data; it is not a chassis dynamometer.
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

R-Speedo adalah dashboard PWA dan Android dengan sepuluh layout yang mengubah ponsel menjadi panel instrumen kendaraan listrik. Aplikasi dapat memakai GPS saja atau membaca telemetri Bluetooth dari controller Votol/Fardriver/VESC, kendaraan Gesits, BMS JK/Daly/ANT/JBD, TPMS BLE, dan modul Polytron ESP32 Votol CAN yang tidak resmi. R-Speedo juga memiliki peta/rute, sesi charging, report perjalanan, multi-battery, motovlog, Dragger, road Dyno, Canvas kustom, Shop hardware Indonesia, live rider, analytics anonim, APK premium, mirror navigasi Cervo, dan widget Android.

Dukungan perangkat tetap bergantung pada model, firmware, adapter, browser, sistem operasi, dan hasil verifikasi nyata. Harga dan metode pembayaran mengikuti flow resmi di aplikasi agar tidak basi.

## Official project

- Website: [r-speedo.app](https://r-speedo.app/)
- Maintainer: [Rasyid Irsyadi](https://github.com/rasyid-irsyadi)
- Corrections: [open an issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues)

R-Speedo is an independent project. References to vehicle, controller, BMS, browser, and platform brands do not imply affiliation or endorsement.

## License and trademarks

Original documentation in this repository is licensed under [Creative Commons Attribution 4.0 International](LICENSE).

The R-Speedo name and logo, third-party trademarks, manufacturer documentation, and third-party media are excluded from that license unless explicitly stated otherwise.
