# Car Parking System — Embedded Systems Project

**Overview**  
An IoT-style parking management prototype that automates barrier control, slot detection, and visual guidance to improve parking efficiency. Implemented as a hardware prototype using Arduino UNO, IR sensors, servo motors, LED indicators, and an I2C LCD for slot display. (See full documentation.) :contentReference[oaicite:2]{index=2}

---

## Key Features
- Automatic entry/exit barrier control using servo motors.
- Real-time detection of cars in each slot via IR sensors.
- LED indicators show slot availability.
- Central LCD displays remaining slots.
- Prevents barrier opening when parking is full.
- Prototype tested in Tinkercad and on a physical model (photos included). :contentReference[oaicite:3]{index=3}

---

## Hardware / Components
- **Microcontroller:** Arduino UNO  
- **Sensors:** Multiple IR proximity sensors (entry, exit, slot detection)  
- **Actuators:** Servo motors for entry and exit barriers  
- **Display:** I2C Liquid Crystal Display (16x2) to show slots left  
- **Indicators:** LEDs for each slot  
- **Misc:** Breadboard, jumper wires, power supply  
(Components list and wiring images in the documentation.) :contentReference[oaicite:4]{index=4}

---

## How it works (high level)
1. Entry IR pair detects incoming vehicle — if a slot is available, entry servo opens briefly and Slot count decrements.  
2. Exit IR pair detects leaving vehicle — exit servo opens and Slot count increments.  
3. Slot IR sensors monitor individual parking spaces and toggle corresponding LEDs (ON = free, OFF = occupied).  
4. LCD continuously shows “Slot Left: X”.  
Code implements debouncing/flags to avoid duplicate triggers (see code snippets). :contentReference[oaicite:5]{index=5}

---

## Prototype & Media
- **Tinkercad simulation:** link referenced in the doc (page 2). :contentReference[oaicite:6]{index=6}  
- **Prototype photos:** wiring and final board shown on pages 3–4. :contentReference[oaicite:7]{index=7}  
- **Video demo:** link included in the documentation (page 4). :contentReference[oaicite:8]{index=8}

---

## Code (summary)
Core logic (from documentation pages 5–8) includes:
- Pin assignments for entry/exit IRs, slot IRs, LEDs, and servos.
- Flags (flag1..flag4) to handle entry/exit sequencing.
- Servo commands to open/close gates and increment/decrement `Slot`.
- Slot LED control based on IR reads.
- LCD updates showing remaining slots.

Refer to `/mnt/data/ES_documentation.pdf` for full code excerpts and wiring diagrams. :contentReference[oaicite:9]{index=9}

---

## Tech Stack
- Arduino (C/C++), Arduino IDE  
- Prototype wiring (breadboard)  
- Tinkercad for simulation and testing

---

## Summary
This project demonstrates practical embedded-system design: sensor integration, actuator control, real-time state handling, and user feedback via LEDs and LCD. The documentation includes circuit diagrams, prototype photos, video demo, and full code snippets for immediate reproduction. :contentReference[oaicite:10]{index=10}

## Video Demonstation
https://drive.google.com/drive/folders/1X0kOunHTpOCDYiS2wK39soh6YYXYTai1?usp=sharing

## TinkerCad
<img width="1477" height="752" alt="image" src="https://github.com/user-attachments/assets/554da770-15df-4fe6-ade6-4682165df0ac" />

