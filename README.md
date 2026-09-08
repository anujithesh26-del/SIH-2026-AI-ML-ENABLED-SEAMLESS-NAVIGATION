# SIH-2026-AI-ML-ENABLED-SEAMLESS-NAVIGATION
# GPS-Denied Vehicle Localization Using Dead Reckoning

This project evaluates vehicle-position estimation during a simulated GPS blackout using:

- **Phone-only inertial dead reckoning** — phone accelerometer and gyroscope data.
- **Vehicle wheel-odometry dead reckoning** — ECU wheel-speed and yaw-rate data.

GPS is used only as ground truth to compare the estimated position after the blackout window.

## Files

| File | Description |
|---|---|
| `data_quality_check.py` | Checks sampling rate, sensor gaps, GPS validity, wheel speeds, and ZUPT behavior. Supports both phone (`S-*.csv`) and vehicle (`V-*.csv`) files. |
| `dead_reckoning_fixed.py` | Phone-only dead reckoning using acceleration, yaw rate, gravity removal, and stationary detection (ZUPT). |
| `dead_reckoning_vehicle.py` | Vehicle dead reckoning using wheel speeds, wheel radius, and ECU yaw rate. |

## Input Data

The scripts use IO-VNBD CSV logs:

- **Phone file:** `S-*.csv`
- **Vehicle ECU file:** `V-*.csv`

Required fields include GPS latitude/longitude, timestamps, and the relevant IMU or vehicle-sensor fields.

## Configuration

Set the simulated GPS-blackout period in all scripts:

```python
WINDOW_START_S = 100
WINDOW_END_S = 150
```

For vehicle odometry, set the approximate wheel radius:

```python
WHEEL_RADIUS_M = 0.30
```

## Workflow

1. Run `data_quality_check.py` to validate the recording.
2. Run `dead_reckoning_fixed.py` with a phone-side CSV.
3. Run `dead_reckoning_vehicle.py` with a vehicle-ECU CSV.
4. Compare the dead-reckoning path against the GPS path and review final position error.

## Outputs

Each dead-reckoning script provides:

- GPS versus estimated 2D trajectory.
- Final position error in metres.
- Error growth over different GPS-outage durations.
- Sensor or speed sanity-check plots.

## Notes

- Phone-only dead reckoning can drift quickly because accelerometer and gyroscope errors accumulate over time.
- Vehicle wheel odometry is generally more stable but can be affected by wheel-radius error and tyre slip.
- Keep the blackout window identical across both methods for a fair comparison.
