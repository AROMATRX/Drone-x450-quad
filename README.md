# Drone-x450-quad
**An open-source, GPS-enabled X-type quadcopter** built on APM 2.8, optimized for stable autonomous missions, failsafe landings, and easy calibration.

# 🛸 X450 Quadcopter Drone Project

![Drone Banner](images/banner.png)

> **An open-source, GPS-enabled X-type quadcopter** built on APM 2.8, optimized for stable autonomous missions, failsafe landings, and easy calibration.

---

## 📖 Table of Contents

1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Hardware Components](#hardware-components)  
4. [Software & Firmware](#software--firmware)  
5. [Folder Structure](#folder-structure)  
6. [Installation & Setup](#installation--setup)  
7. [Calibration & Testing](#calibration--testing)  
8. [Mission Planning](#mission-planning)  
9. [Failsafe & Safety](#failsafe--safety)  
10. [Flight Logs & Analysis](#flight-logs--analysis)  
11. [Troubleshooting](#troubleshooting)  
12. [License & Contributions](#license--contributions)

---

## 📝 Introduction

This repository contains everything you need to build, configure, and operate an **X450 quadcopter** using the **APM 2.8** flight controller. Designed for hobbyists and researchers, it provides:

- **Full parameter set** for autonomous missions  
- **ESC & motor calibration scripts**  
- **Failsafe configurations** for safe landings  
- **Telemetry logging** and post-flight analysis  
- **Comprehensive documentation** for setup, tuning, and troubleshooting  

---

## 🚀 Features

- **Takeoff / Landing** via Mission Planner commands  
- **Loiter**, **AltHold**, **RTL**, and **Auto** flight modes  
- **Auto-land** on low battery or signal loss  
- **GPS-based mission planning** (waypoints, geofencing)  
- **ESC Calibration** & **Motor Test** procedures  
- **Comprehensive logs** for performance tuning  
- **Modular folder structure** for easy extensibility  

---

## 🧩 Hardware Components

| Component            | Model / Specs                         |
|----------------------|----------------------------------------|
| Frame                | X450 Quadcopter Frame (450 mm)         |
| Flight Controller    | APM 2.8                                 |
| GPS + Compass        | Ublox NEO-6M                           |
| ESCs                 | 4 × 30 A SimonK ESCs                   |
| Motors               | 4 × A2212 1000 KV Brushless            |
| Propellers           | 2 × 10×4.5 CW & 2 × 10×4.5 CCW          |
| Battery              | 3S 11.1 V 2200 mAh LiPo                |
| Telemetry            | 433 MHz 3DR Radio Module               |
| Ground Station       | Mission Planner (Windows/Linux/Mac)    |

---

## 💾 Software & Firmware

- **ArduCopter v3.2.1** firmware for APM 2.8  
- **Mission Planner v1.3.49** GCS for Windows  
- **Parameters file**: `firmware/APM-parameters.param`  
- **Optional scripts**: Python & shell scripts for automated uploads

---

## 📂 Folder Structure

