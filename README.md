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
🔍 What is ESC?
ESC means Electronic Speed Controller.
It controls the speed of your drone’s motors.
ESC calibration tells the ESC what is maximum and minimum throttle from your remote.

⚠️ Safety First:
Remove propellers before you start – very important!

Make sure battery is fully charged.

✅ Manual ESC Calibration – Step by Step:
Remove propellers from all motors.

Turn ON your remote controller.

Push the throttle stick to the top (full throttle).

Connect the battery to the APM/drone.

You will hear beep-beep sounds from ESCs.

After the beeping stops, move throttle stick to the bottom (zero throttle).

You will hear a confirmation beep.

ESC Calibration is done! ✅

❗ If ESC calibration is not working:
Check battery connection.

Make sure ESC signal wires are connected properly to APM.

Try one ESC at a time (individual ESC calibration).

Recheck your throttle channel in Mission Planner.
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

✅ Drone Troubleshooting Table (Simple English)
🚨 Problem (Issue)	❓ Why it happens	✅ Easy Solution
Drone arms but motors not spinning	ESC not calibrated or bad connection	Do ESC calibration again and check motor wires
One motor not spinning	ESC or wire problem	Check ESC connection, try swapping ESC to test
Drone lifts but spins in air	Wrong motor order or propeller direction	Fix motor number and propeller direction (CW/CCW)
Drone disarms in air	GPS weak or battery low	Make sure GPS has 6+ satellites and battery is charged
Drone keeps beeping	ESC not calibrated or low battery	Calibrate ESC or check battery voltage
Can't arm drone	Safety checks not passed (like no GPS)	Wait for GPS lock, check Mission Planner for errors
Loiter to Land automatically	GPS weak or failsafe activated	Check GPS signal, make sure HDOP < 2.0
Message action not working	Flight mode not set properly	Set correct flight mode in Mission Planner
ESC calibration not working	Wrong method used	Follow manual ESC calibration (remove props!)
Drone flies then stops mid-air	Power cut or failsafe	Check battery, power module, failsafe settings
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
