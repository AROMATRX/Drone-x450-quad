# Drone-X450 Autonomous Quadcopter Project

## 📌 Overview

This is a fully autonomous quadcopter project based on the **X450 drone frame** using **APM 2.8 flight controller**. The drone supports GPS-based navigation with mission planning using Mission Planner software. It can automatically take off, follow waypoints, loiter, and return to launch (RTL).

---

## 🧰 Hardware Used

| Component                 | Description                               |
| ------------------------- | ----------------------------------------- |
| X450 Drone Frame          | Basic frame for quadcopter                |
| APM 2.8 Flight Controller | Main controller for stabilization & logic |
| GPS Module (Ublox Neo-6M) | For GPS lock and autonomous navigation    |
| ESCs (30A) x4             | Motor speed controllers                   |
| Brushless Motors x4       | For lift and movement                     |
| 1045 Propellers           | For generating lift                       |
| 3S 2200mAh LiPo Battery   | Power source                              |
| FlySky FS-i6 Transmitter  | Manual control                            |


---

## 🖥️ Software Requirements

* **Mission Planner** (for configuration and mission upload)
* **Arduino IDE** (optional for firmware modifications)

---

## 🔧 Configuration Steps

### Step 1: Flash Firmware

* Connect APM 2.8 to PC via USB.
* Open Mission Planner → Initial Setup → Install Firmware → Select ArduCopter v1.3.49.
* links are :- https://firmware.ardupilot.org/Tools/MissionPlanner/archive/MissionPlanner-1.3.49.msi

### Step 2: Sensor Calibration

* Accelerometer Calibration
* Compass Calibration
* Radio Calibration
* Flight Mode Setup (Stabilize, AltHold, Loiter, RTL, Auto)

### Step 3: ESC Calibration (Manual Method)

1. Remove propellers.
2. Turn on transmitter, throttle full.
3. Power APM via battery.
4. Wait for beeps → Throttle down → Calibration done.

---

## ✈️ Flight Modes

| Mode      | Description                      |
| --------- | -------------------------------- |
| Stabilize | Manual flight with auto-leveling |
| AltHold   | Maintains current altitude       |
| Loiter    | GPS hold at a point              |
| Auto      | Executes pre-defined mission     |
| RTL       | Returns to launch location       |

---

## 🗺️ Create Autonomous Mission

1. Open Mission Planner → Flight Plan tab.
2. Right-click on map to add: Takeoff, Waypoint(s), Loiter, Land.
3. Click "Write WPs" to upload to drone.
4. Set flight mode to AUTO → Arm → Fly.

---

## 🧪 Troubleshooting

| Problem                    | Solution                                  |
| -------------------------- | ----------------------------------------- |
| Drone spinning during lift | Check motor order and propeller direction |
| One motor not spinning     | Check ESC connection and solder joints    |
| Disarms automatically      | Check battery voltage and GPS HDOP        |
| Continuous beeping         | ESC not calibrated or low voltage         |

---

## 📂 Project Structure

```
drone-x450/
├── README.md
├── images/                  # Photos & wiring diagrams
├── firmware/                # Parameter files (.param)
├── flight-logs/             # .BIN and .TLOG files
├── scripts/                 # Optional Arduino/Python scripts
└── docs/                    # Setup instructions, manuals
```

---

## 📊 GPS & Telemetry Notes

* HDOP should be **< 2.0** for good GPS lock.
* Minimum 6 satellites required for stable Loiter/Auto mode.

---

## ✅ Final Notes

Make sure to:

* Always calibrate sensors after assembling.
* Keep props removed during motor/ESC test.
* Check direction and position of motors (CW & CCW).
* Set Failsafe modes (RTL for GPS, LAND for battery).

Happy flying! 🚁
