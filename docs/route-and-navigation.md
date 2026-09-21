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

The route estimate combines GPS, vehicle profile, battery/range settings, current telemetry, and map data when available. A route can remain useful with degraded or estimated inputs; missing controller/BMS data does not become fake hardware telemetry.

Charging stations and workshops use local baseline/cache data with optional API refresh. A failed refresh should not erase a valid local baseline or cached result.

## Limits

- ETA, range, energy, and arrival SOC are estimates affected by traffic/data provider, speed, slope, wind, load, battery condition, configuration, and GPS quality.
- Web/PWA map and search behavior depends on network, browser permissions, and map provider availability.
- GPS-only mode cannot know cell voltage, controller current, BMS fault state, or other hardware fields that were never transmitted.
- Community station/workshop information can be incomplete, stale, or awaiting moderation.
- Live-rider sharing is optional and separate from local route/report data and anonymous analytics.

## Related paths

- [Motovlog](motovlog.md) for camera riding workflow.
- [Dragger](dragger.md) for GPS acceleration timing.
- [Road Dyno](road-dyno.md) for setup comparison.
- [Canvas](canvas.md) for a custom dashboard.
