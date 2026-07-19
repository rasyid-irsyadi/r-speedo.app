# EV telemetry guide

Last verified: 2026-07-19

R-Speedo combines data from a phone, motor controller, vehicle module, battery management system, TPMS sensor, and user configuration when those sources are available. The values describe different parts of the vehicle and should not be treated as interchangeable.

## Controller and BMS roles

| Source | Typical responsibility | Example telemetry |
| --- | --- | --- |
| Phone GPS | Position and motion estimate | Speed, route, distance, elevation, heading |
| Motor controller | Motor power delivery and controller state | Electrical speed, current, voltage, temperature, gear/status, faults |
| Vehicle module | Vehicle-specific telemetry bridge | Speed, SOC, odometer, temperatures, voltage/current/capacity, errors |
| BMS | Battery-pack monitoring and protection | Pack voltage/current, state of charge, cell voltages, temperatures, alarms |
| TPMS | Tire pressure monitoring | Pressure, temperature, battery/freshness, warnings |

A field appearing in an app does not prove that every connected device measures it directly. Some values may be estimated, derived, unavailable, or reported with device-specific units and conventions.

## Common values

### Speed

Speed may come from GPS, controller telemetry, or a vehicle module. GPS speed depends on reception, sampling, filtering, and device movement. Controller speed depends on wheel, motor, gearing, pole-pair, and firmware configuration. Compare it with a trusted reference and keep calibration adjustable.

### Voltage

Controller and BMS voltage readings can differ because they may be sampled at different times or points in the electrical system. Wiring loss, load, calibration, and update rate also matter.

### Current and power

Current sign and meaning are device-specific. A positive value may mean discharge on one device and charging or regeneration on another. Approximate electrical power is commonly derived from voltage multiplied by current, but it is not the same as mechanical wheel power.

### State of charge

State of charge is an estimate produced by the BMS, vehicle module, or R-Speedo configuration. Accuracy depends on usable capacity, calibration, current measurement, battery chemistry, balancing, temperature, and whether the BMS has recently reached a known full or empty reference.

### Range

Range is an estimate, not a promise. It changes with recent energy use, speed, terrain, wind, load, temperature, tire pressure, battery condition, and configured capacity.

### Temperature, cell delta, and faults

Temperature fields may refer to different sensors. Cell delta and temperature warnings matter for battery safety, but thresholds and meaning still depend on pack design. Fault codes and protection limits are controller- or BMS-specific. Use the hardware manufacturer's documentation for service decisions.

## GPS-only mode

GPS-only mode is useful when no compatible Bluetooth device is available. It can support:

- Speed and route display.
- Distance and trip timing.
- Basic trip reports.
- Layout 8 Dragger attempts with GPS quality gates.
- Navigation and map features when network data is available.

It cannot reconstruct cell voltages, controller current, internal temperatures, tire pressure, or hardware fault states that were never transmitted to the phone.

The [W3C Geolocation specification](https://www.w3.org/TR/geolocation/) defines the browser geolocation interface but does not guarantee a particular sensor, sampling rate, or accuracy for every device.

## Bluetooth realities

- Wireless packets can be delayed, dropped, duplicated, or interrupted.
- Signal quality changes with phone placement, vehicle structure, interference, and adapter design.
- Device names and protocols can change between firmware or hardware revisions.
- Browsers require user permission and control when Web Bluetooth sessions may start.
- Mobile operating systems can suspend background work to save power.

The [Web Bluetooth specification](https://webbluetoothcg.github.io/web-bluetooth/) describes the browser API. Actual availability still depends on the browser and operating system.

## Multi-battery reality

Multiple packs need more than a combined number on screen. Capacity, voltage range, active/connected state, BMS availability, current direction, and pack visibility affect whether an aggregate is useful. R-Speedo keeps per-pack views and can refuse unsafe aggregation when the inputs are incomplete.

## Dragger timing limits

Layout 8 Dragger uses GPS samples, quality gates, server recomputation, and public evidence to make runs comparable. It still depends on phone GNSS quality, sample intervals, start reconstruction, route shape, elevation, and filtering. Treat it as a practical rider comparison tool, not official timing equipment.

## Calibration and verification

Use a known reference when calibrating speed, wheel size, capacity, current direction, and other vehicle-specific values. Record the hardware model, firmware, test conditions, and R-Speedo settings so a result can be reproduced.

Real hardware is the reference for its own limits. Do not change controller or battery protection settings solely to make two displays agree.

## Safety boundary

R-Speedo is a monitoring and trip-information tool. It does not replace:

- Manufacturer documentation and protection limits.
- A road-legal instrument cluster where required.
- Proper electrical test equipment.
- Inspection and diagnosis by a qualified technician.
- Safe riding decisions.

For integration-specific caveats, see [R-Speedo compatibility](compatibility.md).
