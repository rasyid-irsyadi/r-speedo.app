# R-Speedo privacy notes

Last verified: 2026-07-19

This public repository documents R-Speedo. It does not contain application source code, private backend configuration, account data, payment data, credentials, license tokens, raw user trips, or private endpoints.

## Public media

Screenshots and video in this repository, when present, must use synthetic demo data and public demo locations. They must not show private trip history, home/work locations, real account sessions, payment details, admin screens, browser history, or raw recordings.

## Local data and app data

R-Speedo uses local storage or native app storage for settings, profiles, trip/ODO state, BLE pairing preferences, TPMS state, report data, layout settings, charge session state, Dragger runs/queue, and Android widget snapshots.

Local ride/report data is different from anonymous analytics. A trip can exist locally without being part of analytics export.

## Analytics

Anonymous EV analytics, when enabled according to the current in-app policy, is intended for aggregate product and market-fit insight. It uses an anonymous app-device identifier and privacy guards rather than public rider identity. Sensitive telemetry is reduced before export, and small samples are suppressed by privacy gates.

Live-rider sharing is separate from analytics. It is optional, location-based, and should be understood as a live visibility feature rather than an analytics feature.

## Deletion

R-Speedo provides an in-app deletion-request flow for submitted analytics data. Use the current app flow because the exact UI and policy text can change over time.

## What not to post publicly

Do not post:

- License tokens or account cookies.
- Payment details.
- Credentials or backend configuration.
- Raw GPS traces or location history.
- Screenshots that expose real account, admin, or payment data.
