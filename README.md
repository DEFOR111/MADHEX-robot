# ***MADHEX — Open Source Hexapod Robot***
## 18 DOF · ESP32-S3 · Full custom PCB · CAD included
<img width="892" height="662" alt="WhatsApp Image 2026-07-16 at 12 32 35 PM (1)" src="https://github.com/user-attachments/assets/69723cab-4d20-47e5-8eb7-d186e0f2bae1" />

### ***A fully open-source hexapod project — PCB, CAD  included — for anyone who wants to build their own six-legged walking robot.***

***Features · PCB · CAD & Mechanics · Build Instructions · Gallery · Roadmap · Contributing***

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## ***About:*** 
**MADHEX** is a fully open-source hexapod (six-legged) robot project. It includes a custom-designed power/control PCB, complete mechanical CAD files, and everything needed to build, wire, and bring your own hexapod to life — from soldering the board to your first steps in inverse kinematics.

**This repo is built for makers, robotics students, and hobbyists who want a real, working reference design instead of starting from a blank sheet.**

----------------------------------------------------------------------------------------------------------------------------------
## Features
	
* **18 DOF**	Full range of motion — walk, rotate in place, and climb
* **ESP32-S3-WROOM-1**	Onboard MCU handles inverse kinematics and gait control
* **Custom power PCB**	Compact board with dual buck converters, up to 600 W
* **BNO055 IMU**	Real-time orientation and stability feedback
* **32-channel PWM**	Room to expand with sensors, grippers, or accessories
* **All-terrain** capable	Stable gait tuned for uneven surfaces
* **Fully open**	PCB design, CAD, and build docs — all included

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## PCB
<img width="522" height="416" alt="PCB Top view" src="https://github.com/user-attachments/assets/a5036ce5-c327-4fc9-b50b-f44c781ee181" />

 ***The board is designed to be compact, efficient, and easy to assemble, while still driving 18 servos with headroom to spare.***

### Component	Spec
* Power stage	Dual buck converters, 40 A / up to 600 W combined — stable under peak servo load
* Servo power rails	2 independent lines (J5–J20 = rail A, J21–J36 = rail B) — 9 servos per rail for balanced current draw
* Current sensing	2× INA226 for real-time power monitoring
* PWM outputs	32 channels via 2× PCA9685
* MCU	ESP32-S3-WROOM-1 — inverse kinematics + gait control
* IMU	BNO055 — orientation, balance, stability
* Logic supply	AMS1117 3.3 V regulator
* I/O	USB-C, 2× SMD buttons

***Why it matters:*** **a small footprint board that reliably drives 32 PWM channels means more room in the chassis for batteries, sensors, or a gripper — without redesigning the electronics.**

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
## CAD 
<img width="1008" height="688" alt="WhatsApp Image 2026-07-16 at 12 32 35 PM (2)" src="https://github.com/user-attachments/assets/25f35361-2b33-45ec-b60d-fe705a514797" />

| Spec | Value |
| :--- | :--- |
| **Size** | ~800 mm length × 300 mm height |
| **Servos** | DS3235 (high-torque, no secondary shaft) |
| **Shaft support** | Added bearings on each joint to compensate for the single-shaft servo design, reducing backlash and improving long-term stability |
| **Range of motion** | Mid-to-high performance angle range, tuned for smooth walking gait |

## building Instruction 

<img width="1341" height="1600" alt="WhatsApp Image 2026-07-20 at 11 35 21 PM" src="https://github.com/user-attachments/assets/08fcf0c4-6c22-4a2e-aecc-bed97bb3adfc" />

* Print/order the chassis — CAD files in /cad
* Assemble the PCB — schematics and Gerbers in /pcb
* Wire the servos — respect the two power rails (9 servos per rail)
