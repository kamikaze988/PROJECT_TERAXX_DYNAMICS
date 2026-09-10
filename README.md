PROJECT TERAXX DYNAMICS — TERAXX X-CORE

TERAXX X-CORE is an ESP32-based off-road RC basher project focused on combining high-performance RC control, custom electronics, telemetry, and software into one platform.

The system uses an ESP32 as the vehicle controller and supports a PS4 gamepad for wireless control. The project also includes a custom web-based dashboard for monitoring and controlling the vehicle.

CURRENT FEATURES
 PS4/PS3 wireless gamepad control,
 Analog steering,
 Mobile-friendly web control interface,
 Tilt steering mode,
 Adjustable steering sensitivity,
 Steering dead zone,
 180° servo steering,
 Servo smoothing,
 Throttle / reverse control,
 precision / beast driving modes,
 active-aero spoiler control logic,
 backflip/front flip jump control with the right analog joystick,
 Boost mode,
 Wheelie control,
 Halo lighting control,
 Roof/accessory control,
 Live telemetry,
 Battery-voltage monitoring,
 Speed/RPM display,
 Performance graph,
 Gamepad connection failsafe logic,
 adaptive low voltage cutoff logic,
 GPS Return-to-Home logic,
 ESP32 web dashboard,
 Keyboard control support,
 Failsafe System,

TERAXX X-CORE includes a failsafe system designed to react when the controller connection is lost. If the connection remains lost beyond the configured timeout, the vehicle enters its failsafe/Return-to-Home behavior rather than simply continuing with the last control input.

STEERING SYSTEM

The steering system supports both:

NORMAL MODE

PS4 analog stick steering,
Adjustable dead zone,
Adjustable sensitivity,
Servo smoothing,

TILT MODE

Uses the controller's accelerometer,
Configurable tilt dead zone,
Adjustable steering sensitivity (with the Dpad buttons),
Converts controller movement into steering commands,

WEB DASHBOARD 

The ESP32 hosts a custom TERAXX DYNAMICS dashboard featuring:

Real-time gauges,
Speed display,
RPM estimation,
Battery voltage,
Steering controls,
Throttle/reverse controls,
Boost and wheelie controls,
Halo and roofligth controls,

AERO DYNAMICS (active spoiler/backflip and front flip)

The esp32 aero logic turns the right analog joystick inputs to throttle/braking commands therefore enabling backflips and front flips.
While for the active spoiler esp32 controls a servo motor's degree which controls the spoiler which adapts to the boost, brake, backflip logic

🧠 PROJECT GOAL

The goal of TERAXX X-CORE isn't simply to build another RC car.

It's an experiment in combining RC hardware, embedded programming, wireless controllers, vehicle telemetry, safety systems, and a custom user interface into rc vehicle platform.

For more info drop comments 

Bashing Beyond Crashing.
