# R-Speedo reports and data

Last verified: 2026-09-21

R-Speedo reports turn ride telemetry into local evidence that can help riders understand range, energy use, charging, setup quality, and hardware behavior. Reports are not lab-grade measurement and are not a sales forecast.

## Trip summary

A report can include distance, top speed, average speed, moving time, trip duration, state-of-charge used, Ah/Wh consumption, regeneration, charge evidence, estimated cost, efficiency, CO2 comparison, and source quality when the required data is available.

Missing telemetry should be read as unavailable, not as zero. GPS-only trips cannot include controller current, cell delta, BMS alarms, or pack-level details that were never captured.

## Route evidence

Route evidence can include GPS points, route map, stops, charging context, workshop context, and timing. GPS accuracy depends on phone hardware, placement, sky visibility, sampling interval, filtering, and background behavior.

## Telemetry charts

Charts may include speed, GPS speed, RPM, voltage, current, SOC, cell delta, temperature, elevation, pitch/roll, and efficiency. Chart availability depends on what the phone and connected hardware provided during the trip.

## Multi-battery reporting

Multi-battery reports can show pack summaries, connected/estimated/active state, pack visibility, current per pack when available, warnings, and aggregate values. Aggregates can be rejected or degraded when pack data is incomplete or unsafe to combine.

## Controller tuning evidence

Controller tuning is protocol-specific. Reports and road Dyno comparisons can preserve the selected vehicle profile and available controller-setting snapshot so a rider can relate a measured result to a setup change. This is context for comparison, not proof that every field was writable or that the change alone caused the result.

Votol and confirmed Fardriver fields may be writable through the Controller panel. VESC, Gesits, Polytron, and SFOX350 paths remain read-only or diagnostic where stated. Layout 9 never writes controller settings.

## Charge sessions

Charge session views can show SOC, ETA, energy added, Ah/kWh, estimated cost, voltage, temperature, and cell-delta warnings. ETA and cost depend on telemetry quality, charger behavior, configured capacity, nominal voltage, tariff settings, and whether current is measured or inferred.

## Dragger evidence

Layout 8 Dragger can produce GPS-based split timing for 60ft, 100m, 201m, 301m, 402m, and 0-60/100/120 km/h. Eligible runs are recomputed server-side for leaderboard submission. Public evidence can include quality indicators, start model, GPS rate/accuracy, power/class evidence, two-way badge, and coordinate-free public traces.

Raw coordinates are not part of the public evidence view. They are retained only for limited moderation needs and can be removed by retention logic.

## Motovlog evidence

Layout 7 can pair a riding video with a telemetry sidecar or overlay, snapshots, gallery state, and exported media. Video quality, storage, background behavior, audio, and platform support vary by browser, Android, iOS, camera, and available space.

## Road Dyno data

Layout 9 road Dyno keeps its pull analysis local. It can compare paired two-way pulls and show readiness/cooldown state, time, energy, voltage sag, temperature, and minimum wheel-power/torque estimates when the required data is available. Baseline and candidate comparisons can help evaluate setup changes.

These results depend on road, wind, slope, vehicle mass/configuration, GNSS, sampling, and source telemetry. They are practical road estimates, not laboratory or chassis-dyno measurements, and they do not change controller settings.

## Export formats

R-Speedo report export supports:

- `PNG` for a visual report image.
- `CSV` for tabular trip data.
- `GPX` for route data when GPS route points exist.
- `JSON` for complete report data.

Exports come from local trip/report data and do not require analytics opt-in.

## Privacy boundary

Local reports, anonymous analytics, live-rider sharing, and public demo media are separate concepts. Public repository media must use synthetic or intentionally public demo data and public locations. Anonymous analytics exports are aggregate signals, not raw user reports.
