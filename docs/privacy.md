# R-Speedo privacy notes

Last verified: 2026-09-21

This public repository documents R-Speedo. It does not contain application source code, private backend configuration, account data, payment data, credentials, license tokens, raw user trips, or private endpoints.

## Public media

Screenshots and video in this repository are copied from the media folder supplied by the R-Speedo maintainer for public documentation and marketing.

## Local data and app data

R-Speedo uses local storage or native app storage for settings, profiles, trip/ODO state, BLE pairing preferences, TPMS state, report data, layout settings, charge session state, Dragger runs/queue, road Dyno runs/baselines, custom Canvas configurations and selected local image assets, and Android widget snapshots.

Local ride/report data is different from anonymous analytics. A trip can exist locally without being part of analytics export. Controller-setting snapshots, tuning context, multi-battery configuration, and road Dyno baselines may also remain local to support comparison without publishing raw account data.

## Analytics

Anonymous EV analytics, when enabled according to the current in-app policy, is intended for aggregate product and market-fit insight. It uses an anonymous app-device identifier and privacy guards rather than public rider identity. Sensitive telemetry is reduced before export, and small samples are suppressed by privacy gates.

Live-rider sharing is separate from analytics. It is optional, location-based, and should be understood as a live visibility feature rather than an analytics feature.

## Deletion

R-Speedo provides an in-app deletion-request flow for submitted analytics data. Use the current app flow because the exact UI and policy text can change over time.
