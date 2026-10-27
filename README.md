<div align="center">
  <h1>🏎️ PROJECT TERAXX DYNAMICS — TERAXX X-CORE</h1>
  <h3><i>"Bashing Beyond Crashing."</i></h3>
  <p>An ESP32-powered, custom-built 2WD off-road RC basher featuring real-time sensor fusion, auto-leveling, and a live web telemetry HUD.</p>
</div>

---

## 📖 About The Project
TERAXX X-CORE isn't just another RC car. It is an experiment in combining custom mechanical fabrication, embedded programming, wireless controllers, vehicle telemetry, and safety systems into one unified platform.

The system uses an **ESP32** as the central vehicle controller, completely replacing a traditional RC receiver. It supports a PS4 gamepad for wireless control, hosts a custom mobile-friendly Web Dashboard, and utilizes an MPU6050 gyro for advanced driving dynamics.

---

## 📸 Build Gallery
*(Note: The first two are your linked images, replace the others with your uploaded photos)*

| Chassis Top View | Chassis Bottom View |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/ec231d14-18c6-44ef-8ce1-99e4e9facabe" width="400" /> | <img src="https://github.com/user-attachments/assets/5c8d36a8-19ca-457d-af12-43110925bdbd" width="400" /> |

| Custom PVC Boom & Aluminum Pan | Cardboard Body Shell (Front) |
|:---:|:---:|
| <img src="[PASTE IMAGE URL HERE]" width="400" /> | <img src="[PASTE IMAGE URL HERE]" width="400" /> |

<div align="center">
  <img src="[PASTE IMAGE URL HERE]" width="600" />
</div>

---

## ✨ Current Features

### 🎮 Control & Steering
*   **PS4/PS3 Wireless Gamepad** control via Bluetooth.
*   **Normal Mode:** Analog stick steering with adjustable dead zone and sensitivity.
*   **Tilt Mode:** Uses the controller's accelerometer to steer.
*   **Web/Mobile Control:** Alternative driving interface via the ESP32 Web Dashboard.
*   **Keyboard Control** support.
*   **Servo Smoothing:** Prevents jerky steering movements.

### ⚡ Performance & Driving Dynamics
*   **Precision & Beast Modes:** Toggle between limited power and full 950 PWM throttle.
*   **Boost & Wheelie Control:** Instant power surges and wheelie bursts.
*   **Aerodynamics & Flips:** The ESP32 reads the right analog joystick to command throttle/braking, enabling mid-air **Backflips and Frontflips**.
*   **Active Aero (Spoiler):** A servo-driven spoiler that adapts dynamically to boost, braking, and jump logic.

### 📊 Telemetry & Web Dashboard
*   The ESP32 hosts a custom, mobile-friendly web HUD.
*   Live battery-voltage monitoring.
*   Speed/RPM display with a performance graph.
*   Real-time gauges and steering/throttle controls.

### 🛡️ Safety & Failsafes
*   **Gamepad Connection Failsafe:** If the Bluetooth connection drops, the car stops.
*   **GPS Return-to-Home (RTH):** If the signal is lost beyond the timeout, the car uses GPS to navigate back to its starting point.
*   **Adaptive Low Voltage Cutoff (LVC):** Protects the LiPo battery from over-discharging with soft and hard power cuts.

### 💡 Accessories
*   Halo lighting control.
*   Roof/accessory light control.

---

## ⚙️ System Deep Dive

### 🛞 The Steering Pipeline
The steering system supports both analog stick control and tilt control. In Normal Mode, the ESP32 applies an exponential curve (Expo) to the analog stick input to soften the center feel, combined with a **Gyro Yaw Assist** that counter-steers when the rear tires lose traction.

### 🌐 The Web Dashboard
The ESP32 acts as a WiFi Access Point. Connect to it from any smartphone to access the TERAXX DYNAMICS dashboard, where you can see real-time speed, battery voltage, and even drive the car if your gamepad dies.

### 🛡️ Failsafe Logic
Safety is built into the core loop. If the controller disconnects for more than 1.5 seconds, the system automatically engages the GPS Return-to-Home logic, steering the car back toward the home coordinates locked at boot.

---

## 🎯 Project Goal
The goal of TERAXX X-CORE is to push the boundaries of what a DIY hobbyist platform can do. By bringing drone-level sensor fusion and telemetry into a ground RC vehicle, we create a machine that is faster, smarter, and safer than off-the-shelf bashers. 

**For more info, drop comments or open an Issue!**

---
<div align="center">
  <b>Built with ⚙️ and ☕ by a builder who refuses to just buy a Traxxas.</b>
</div>![Uploading 1000496301.jpg…]()
<img width="4064" height="3048" alt="1000509648" src="https://github.com/user-attachments/assets/8feb21c2-349e-4c75-801f-bc895076d9f8" />
<img width="3048" height="4064" alt="1000517797" src="https://github.com/user-attachments/assets/aee77713-2ecc-4aac-9458-32387533c4a6" />
