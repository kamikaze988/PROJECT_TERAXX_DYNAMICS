TITLE: PROJECT_TERAXX_DYNAMICS (THE X-CORE VERSION)
AUTHOR: KAMIKAZE
Description: TERAXX X-CORE is a scratch-built  RC car that uses custom ESP32 to process c++ logic and signals. this firmware  bridges the gap between hobbyist vehicle and autonomous robotics.
progress: 70%.  
stil need parts like a 45-50 cm differential drivetrain for the double rear wishbone suspension.25T motor with a 2s battery and a 180 servo then some halo led light. I've been working on it since September first but I'll give you guys the update from October 15th.

October 15th - 3 Hours

· Goal: Upgrade from the flexing plastic chassis to a PVC pipe chassis.
· What I did: Built a new PVC pipe and mounted all the components<img width="3048" height="4064" alt="1000881056" src="https://github.com/user-attachments/assets/816d0473-d6ff-4f47-818d-cdb03c97592f" />
<img width="3048" height="4064" alt="1000881060" src="https://github.com/user-attachments/assets/67928632-523b-405d-8d73-7842ece48f39" />
<img width="3048" height="4064" alt="1000881061" src="https://github.com/user-attachments/assets/4337efbd-d96b-49ec-b187-02451012fab0" />
· Challenges: the steering linkages were binding. 
fix: I recalibrated the steering linkages and the bellcrank system. I also add Ackerman steering for better and smoother conering in turns

October 20th - 4 Hours

· Goal: Integrate Auto-Leveling.
· What I did: Added the accelerometer read to the MPU6050 code. Wrote a PD control loop to nudge the throttle when the car is nose-up.
· Challenges: The manual joystick and the auto-level were fighting each other. I fixed it by snapping the Air adjust to zero when the stick is centered. but it was resolved only on the software part, I'll still need to test it on the ramps with the PS4 gamepad. 
