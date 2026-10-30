<div align="center">
  <h1> PROJECT TERAXX DYNAMICS — TERAXX X-CORE</h1>
  <h3><i>"Bashing Beyond Crashing."</i></h3>
  <p>An ESP32-powered, custom-built 2WD off-road RC basher featuring real-time sensor fusion, auto-leveling, and a live web telemetry HUD.</p>
</div>

---

##  About The Project
TERAXX X-CORE isn't just another RC car. It is an experiment in combining custom mechanical fabrication, embedded programming, wireless controllers, vehicle telemetry, and safety systems into one unified platform.

The system uses an **ESP32** as the central vehicle controller, completely replacing a traditional RC receiver. It supports a PS4 gamepad for wireless control, hosts a custom mobile-friendly Web Dashboard, and utilizes an MPU6050 gyro for advanced driving dynamics.

---

##  Build Gallery

| PVC Chassis bottom  View | PVC Chassis Bottom View |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/ec231d14-18c6-44ef-8ce1-99e4e9facabe" width="400" /> | <img src="https://github.com/user-attachments/assets/5c8d36a8-19ca-457d-af12-43110925bdbd" width="400" /> |

| Cardboard Body Shell side view (1)| Cardboard Body Shell front view (2)
|Cardboard Body Shell rear view(3) |
| <img src="https://github.com/user-attachments/assets/8feb21c2-349e-4c75-801f-bc895076d9f8" width="400" /> | <img src="https://github.com/user-attachments/assets/aee77713-2ecc-4aac-9458-32387533c4a6" width="400" /> |<img width="4064" height="3048" alt="1000501407" src="https://github.com/user-attachments/assets/f710a33d-795a-4fb4-be2c-3d8b49c9eab9" />


---

##  Current Features

###  Control & Steering
*   **PS4/PS3 Wireless Gamepad** control via Bluetooth.
*   **analog steering Mode:** Analog stick steering with adjustable servo responsiveness and sensitivity.
*   **Tilt steering Mode:** Uses the controller's accelerometer to steer, ignoring analog steering inputs at this point.
*   **Web/Mobile Control:** Alternative driving interface via the ESP32 Web Dashboard.
*   **Keyboard Control** support.
*   **Servo Smoothing:** Prevents jerky steering movements.

###  Performance & Driving Dynamics
*   **Precision & Beast Modes:** Toggle between limited power and full 950 PWM throttle.
*   **Boost & Wheelie Control:** Instant power surges and wheelie bursts.
*   **Aerodynamics & Flips:** The ESP32 reads the right analog joystick to command throttle/braking, enabling mid-air **Backflips and Front flips**.
*   **Active Aero (Spoiler):** A servo-driven spoiler that adapts dynamically to boost, braking, and jump logic.

###  Telemetry & Web Dashboard
*   The ESP32 hosts a custom, mobile-friendly web HUD.
*   Live battery-voltage monitoring.
*   Speed/RPM display with a performance graph.
*   Real-time gauges and steering/throttle controls.

###  Safety & Failsafes
*   **Gamepad Connection Failsafe:** If the Bluetooth connection drops, the car stops.
*   **Adaptive Low Voltage Cutoff (LVC):** Protects the LiPo battery from over-discharging with soft and hard power cuts.

###  Accessories
*   Halo lighting control.
*   Roof/accessory light control.

---

##  System Deep Dive

###  The Steering Pipeline
The steering system supports both analog stick control and tilt control. In analog steer Mode, the ESP32 applies an exponential curve (Expo) to the analog stick input to soften the center feel, combined with a **Gyro Yaw Assist** that counter-steers when the rear tires lose traction.

###  The Web Dashboard
The ESP32 acts as a WiFi Access Point. Connect to it from any smartphone to access the TERAXX DYNAMICS dashboard, where you can see real-time speed, battery voltage, and even drive the car if your gamepad dies.

###  Failsafe Logic
Safety is built into the core loop. If the controller disconnects for more than 1.5 seconds, the car comes to a complete halt, completely canceling any loop or logic that may activate when the gamepad is disconnected.

---

##  Project Goal
The goal of TERAXX X-CORE is to push the boundaries of what a DIY hobbyist platform can do. By bringing drone-level gyro and accelerometer assistance and telemetry into a ground RC vehicle, I will create a machine that is more fun, smarter, and safer than off-the-shelf bashers. 

**For more info, drop comments or open an Issue!**

##  Support the TERAXX X-CORE Build

If you'd like to support this project, you can send **USDT (TRC-20)** here:
`TDD4eFM4tTyYeuL4TDLT4PW379f2hFdfM7`

---
<div align="center">
  <b>Built from scratch and inspired by a builder who refuses to just buy a Traxxas.</b>
</div>
