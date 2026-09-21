# Route and navigation

## What this path is for

Layout 6 and the Route panel help a rider plan a trip, understand energy needs, and find support along the way. This is the navigation path, separate from Motovlog, Dragger, Road Dyno, and Canvas.

## What it can do

- Search or open a destination link.
- Show route distance, estimated time, timeline, cost context, and energy/SOC profile.
- Suggest charging stops with arrival SOC, target SOC, safety margin, and charging duration context when the required vehicle data is available.
- Show charging stations and community workshops around the route.
- Show optional live-rider context.
- Mirror time and navigation instructions to a supported Alva Cervo BL-CERVO head unit.
- Work in GPS-only mode for route, distance, map, and basic trip planning when BLE hardware is unavailable.

## Data behavior

The route estimate combines GPS, vehicle profile, battery/range settings, current telemetry, and map data when available. Hardware fields appear when their controller/BMS sources are connected; route planning remains useful with estimated inputs.

Charging stations and workshops combine available device data with refreshed community information. A refresh problem leaves the rider with the last useful result when one is available.

## Limits

- ETA, range, energy, and arrival SOC are estimates affected by traffic/data provider, speed, slope, wind, load, battery condition, configuration, and GPS quality.
- Web/PWA map and search behavior depends on network, browser permissions, and map provider availability.
- GPS-only mode focuses on location, motion, route, and trip data; cell voltage, controller current, BMS fault state, and other hardware fields appear when transmitted by compatible hardware.
- Community station/workshop information can be incomplete, stale, or awaiting moderation.
- Live-rider sharing is optional and separate from local route/report data and anonymous analytics.

## Related paths

- [Motovlog](motovlog.md) for camera riding workflow.
- [Dragger](dragger.md) for GPS acceleration timing.
- [Road Dyno](road-dyno.md) for setup comparison.
- [Canvas](canvas.md) for a custom dashboard.
