# R-Speedo

R-Speedo is a PWA and Android dashboard that turns a phone into an EV instrument panel using GPS and optional Bluetooth telemetry from supported motor controllers and battery management systems.

[Open R-Speedo](https://r-speedo.app/) · Last verified: 2026-07-01 · Current app version: 1.0.10

## What R-Speedo does

- Shows speed, battery, controller, trip, and navigation information in six dashboard layouts.
- Reads supported Votol and Fardriver motor controllers over Bluetooth.
- Reads supported JK, Daly, and ANT battery management systems (BMS) over Bluetooth.
- Works in GPS-only mode when no compatible Bluetooth hardware is available.
- Provides route planning, trip reports, charging-station data, and optional live-rider sharing.
- Supports multiple configured battery packs and BMS connections.
- Runs as a web/PWA app and as an Android APK with native Bluetooth and background capabilities.

## Supported integrations

| Category | Integration | Status |
| --- | --- | --- |
| Motor controller | Votol | Integrated |
| Motor controller | Fardriver | Integrated |
| BMS | JK | Integrated |
| BMS | Daly | Integrated |
| BMS | ANT | Integrated |
| Vehicle profile | Polytron with an external ESP32 Votol CAN module | Experimental and unofficial |

An integrated brand or protocol is not a guarantee that every model, firmware version, or third-party Bluetooth adapter will work. See the [compatibility notes](docs/compatibility.md) before choosing hardware.

## Important limitations

- Web/PWA Bluetooth requires a browser and operating system that implement the Web Bluetooth API.
- GPS-only mode cannot provide controller, cell, fault, or other BMS telemetry.
- Mobile operating systems may suspend browser activity in the background; the Android APK provides additional native background support.
- Charging-station coverage and community data can be incomplete or outdated.
- Polytron integration requires an external unofficial module and does not support writing controller settings.
- R-Speedo is a monitoring aid, not a replacement for manufacturer limits, calibrated instruments, or safe riding practices.

## Documentation

- [Product overview](docs/product.md)
- [Hardware and platform compatibility](docs/compatibility.md)
- [Frequently asked questions](docs/faq.md)
- [EV telemetry guide](docs/ev-telemetry-guide.md)

## Ringkasan Bahasa Indonesia

R-Speedo adalah dashboard PWA dan Android yang mengubah ponsel menjadi panel instrumen kendaraan listrik. Aplikasi dapat memakai GPS saja atau membaca telemetri Bluetooth dari controller Votol/Fardriver dan BMS JK/Daly/ANT yang kompatibel. Integrasi Polytron memakai modul ESP32 Votol CAN eksternal yang tidak resmi. Dukungan perangkat tetap bergantung pada model, firmware, adapter, browser, dan sistem operasi.

## Official project

- Website: [r-speedo.app](https://r-speedo.app/)
- Maintainer: [Rasyid Irsyadi](https://github.com/rasyid-irsyadi)
- Corrections: [open an issue](https://github.com/rasyid-irsyadi/r-speedo.app/issues)

R-Speedo is an independent project. References to vehicle, controller, BMS, browser, and platform brands do not imply affiliation or endorsement.

## License and trademarks

Original documentation in this repository is licensed under [Creative Commons Attribution 4.0 International](LICENSE).

The R-Speedo name and logo, third-party trademarks, manufacturer documentation, and third-party media are excluded from that license unless explicitly stated otherwise.
