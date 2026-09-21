# Road Dyno

## What this path is for

Layout 9 is a local setup-comparison tool for riders and tuners. It answers “did this change help under comparable road conditions?” It is not a chassis dynamometer and it does not write controller settings.

## The tuning loop

1. Choose the test goal: acceleration, upper speed, efficiency, or balanced.
2. Set the speed range, vehicle/test mass, and available safety limits.
3. Check readiness: stopped state, speed source, hard limits, GPS, mounting, telemetry, cooldown, grade, and pairing evidence.
4. Perform one or more road pulls; paired directions can reduce slope/wind bias.
5. Review measured time, energy, current, voltage sag, temperature, curve, and source quality.
6. Save a baseline, compare a candidate, and use guidance only when the evidence supports it.

## Measured versus estimated

Battery electrical power can be measured/derived from voltage and current. Minimum wheel-power/torque is an estimate from available road, vehicle, GPS, and telemetry evidence. The result is not a certified dyno number.

The Controller panel remains the place for supported settings writes. Layout 9 can use a controller-setting snapshot as comparison context but never changes the controller itself.

## Limits

Road, wind, slope, mass/configuration, tire condition, GNSS, sampling, mounting, cooldown, sensor calibration, and traffic all affect repeatability. A low-confidence result should degrade to measurement/retest instead of pretending to be precise.

## Related paths

- [Dragger](dragger.md) for acceleration timing and leaderboard comparison.
- [Reports and data](reports-and-data.md) for evidence/export.
- [Controller tuning](compatibility.md) for protocol and writable-field boundaries.
