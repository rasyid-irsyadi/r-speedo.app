# R-Speedo reports and data

Last verified: 2026-07-19

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

## Charge sessions

Charge session views can show SOC, ETA, energy added, Ah/kWh, estimated cost, voltage, temperature, and cell-delta warnings. ETA and cost depend on telemetry quality, charger behavior, configured capacity, nominal voltage, tariff settings, and whether current is measured or inferred.

## Dragger evidence

Layout 8 Dragger can produce GPS-based split timing for 60ft, 100m, 201m, 301m, 402m, and 0-60/100/120 km/h. Eligible runs are recomputed server-side for leaderboard submission. Public evidence can include quality indicators, start model, GPS rate/accuracy, power/class evidence, two-way badge, and coordinate-free public traces.

Raw coordinates are not part of the public evidence view. They are retained only for limited moderation needs and can be removed by retention logic.

## Export formats

R-Speedo report export supports:

- `PNG` for a visual report image.
- `CSV` for tabular trip data.
- `GPX` for route data when GPS route points exist.
- `JSON` for complete report data.

Exports come from local trip/report data and do not require analytics opt-in.

## Privacy boundary

Local reports, anonymous analytics, live-rider sharing, and public demo media are separate concepts. Public repository media must use synthetic data and public locations. Anonymous analytics exports are aggregate signals, not raw user reports.
