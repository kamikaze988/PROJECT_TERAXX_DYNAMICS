# 🏎️ PROJECT TERAXX DYNAMICS — TERAXX X-CORE

**Bashing Beyond Crashing.**

TERAXX X-CORE is a scratch-built, ESP32-powered 1/18 scale off-road RC basher. It is an experiment in combining embedded programming, real-time sensor fusion, custom electronics, and a live web interface into a single custom vehicle platform. 

Unlike off-the-shelf RC cars, this build replaces proprietary radio systems with an ESP32 microcontroller, allowing for advanced features like gyro-assisted steering, auto-leveling, and GPS Return-to-Home.

## 📸 Gallery

<div align="center">
  <img src="https://github.com/user-attachments/assets/ec231d14-18c6-44ef-8ce1-99e4e9facabe" width="45%" />
  <img src="https://github.com/user-attachments/assets/5c8d36a8-19ca-457d-af12-43110925bdbd" width="45%" />
</div>
<br>
<div align="center">
  <i>Custom aluminum pan chassis, PVC structural spine, and DIY cardboard body with LED bar.</i>
</div>

---

## ⚡ Core Features

### 🎮 Control & Drive
*   **Wireless Input:** PS4/PS3 gamepad control via Bluepad32 (with Zero-latency BT).
*   **Dual Steering Modes:** Normal analog stick steering, plus a "Tilt Steering" mode that uses the controller's internal accelerometer.
*   **Driving Profiles:** Switch between "Precision" (smooth, controlled) and "Beast" (maximum throttle and aggressive dynamics) modes.
*   **Action Buttons:** Dedicated boost mode, wheelie control, and adjustable steering sensitivity/response on the fly.

### 🧠 Smart Systems & Physics (Firmware)
*   **Auto-Leveling Assist:** Uses an MPU6050 IMU and a complementary filter to calculate pitch angle mid-air. A PD control loop automatically levels the car if the driver releases the right analog stick. *(Disabled during wheelies).*
*   **Gyro-Assisted Counter-Steering:** Automatically counter-steers when the rear end slides out, keeping the car straight on loose dirt.
*   **Aero Dynamics & Flips:** Logic that translates right analog stick inputs into precise throttle/brake pulses to execute mid-air backflips and frontflips. *(Also includes an active aero spoiler servo).*
*   **GPS Return-to-Home (RTH):** If the Bluetooth signal drops, the ESP32 calculates the heading via GPS and navigates the car back toward the home coordinates.

### 📊 Telemetry & Interface
*   **ESP32 Web HUD:** The car broadcasts its own WiFi network. Connect to it to view a live, draggable dashboard featuring speed/RPM, battery voltage, steering controls, and active telemetry.
*   **Safety Failsafes:** Multi-tier adaptive Low Voltage Cutoff (LVC) to protect the LiPo battery, and connection-loss failsafes.
*   **Black-Box Logging:** *(Coming Soon)* SD card integration for high-frequency telemetry tracking.

---

## ⚙️ System Architecture

The brain of the car is an **ESP32**, which handles multiple tasks simultaneously using FreeRTOS:
1.  **Bluetooth Classic:** Receiving PS4 controller data.
2.  **WiFi & WebServer:** Hosting the HTML/JS dashboard and handling telemetry requests.
3.  **I2C Bus:** Polling the MPU6050 for real-time gyro (yaw) and accelerometer (pitch) data.
4.  **UART:** Parsing NMEA sentences from the GPS module.
5.  **PWM:** Controlling the ESC, Steering Servo, and Aero Spoiler.

## 🛠️ Hardware Stack
*   **MCU:** ESP32 (Dual-Core)
*   **Chassis:** Custom aluminum pan + PVC pipe structural spine (for torsional rigidity).
*   **Sensors:** MPU6050 (IMU), NEO-6M (GPS).
*   **Actuators:** 180° Steering Servo, Brushed ESC + Motor, Aero Spoiler Servo.

---

## 🧠 Project Goal
The goal of TERAXX X-CORE isn't simply to build another RC car. It's an experiment in pushing cheap RC hardware to its absolute limits through embedded programming and real-time physics calculations. It is a testbed for safety systems, telemetry, and custom user interfaces.

*For more info, check out the [JOURNAL.md](JOURNAL.md) to see the build process!*
