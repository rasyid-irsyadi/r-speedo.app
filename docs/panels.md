# App panels and supporting workflows

Layouts are only one part of R-Speedo. These panels provide the setup, health, data, purchase, and community workflows around the dashboards.

| Panel/workflow | Main job |
| --- | --- |
| Wizard | First-run profile, permissions, BLE pairing, defaults, and getting a rider to a usable dashboard |
| Controller | Live controller monitor plus protocol-specific settings/tuning where safe writes are supported |
| BMS | Pack SOC, voltage, current, power, temperature, cell grid, delta, SOH, cycles, alarms, and multi-pack views |
| Charge | Active/completed charging session, ETA, energy, cost, voltage, temperature, and cell warnings |
| Route | Destination, map, route timeline, energy profile, charging/workshop context, and live rider |
| Report | Calendar/trip history, route map, charts, data quality, performance, battery, energy, cost, and export |
| Settings | Vehicle profiles, calibration, source selection, layout controls, storage, language, privacy, and device behavior |
| Premium/account | Google login, Pass/Lifetime access, devices, APK release/update state, license, and account deletion |
| Shop | Indonesia-only hardware catalog, compatibility context, availability, IDR price, images, and WhatsApp handoff |
| Hall of Fame | Opt-in monthly distance/elevation/efficiency boards and rider identity presentation |

The panels are shared infrastructure around the layout paths: a rider can use GPS-only features without BLE, configure multiple packs without losing per-pack visibility, and keep local reports even when network synchronization is unavailable.
