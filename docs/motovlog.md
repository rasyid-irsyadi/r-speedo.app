# Motovlog

## What this path is for

Layout 7 is a riding-vlog workflow: record the ride and keep useful EV telemetry with the video. It is separate from the Route/navigation, Dragger, Road Dyno, and Canvas paths.

## What it can do

- Camera preview and recording.
- Pause, resume, and snapshot capture.
- Gallery browsing and recording retention.
- Bluetooth intercom microphone support where the platform exposes it.
- Telemetry sidecar/export and overlay context for speed, battery, controller, GPS, and temperature fields that were available during the ride.
- Web/native storage and sharing paths.
- Android MP4 remux without re-encoding where the recording and device path support it, plus safe replacement before playback/share.

Layout 7 assets may require an authenticated R-Speedo session. Android has the deepest native file and background integration; browser and iOS behavior depends on platform storage, camera, microphone, and lifecycle limits.

## What the video does not prove

Video telemetry is evidence of what the phone received, not a laboratory measurement. Missing BLE frames, GPS gaps, camera clock differences, sensor calibration, and background suspension can make the overlay or sidecar incomplete.

## Limits

- Camera, microphone, Bluetooth intercom, storage, file playback, and sharing depend on browser/OS permissions and device capabilities.
- Large recordings can exceed browser/WebView memory or origin-storage limits.
- A video with telemetry does not replace the original controller/BMS report or manufacturer diagnostics.

## Related paths

- [Route and navigation](route-and-navigation.md) for trip planning.
- [Reports and data](reports-and-data.md) for interpretation and exports.
- [Canvas](canvas.md) for custom telemetry dashboards.
