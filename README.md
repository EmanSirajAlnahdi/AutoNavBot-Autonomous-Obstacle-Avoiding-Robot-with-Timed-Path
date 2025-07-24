# AutoNavBot-Autonomous-Obstacle-Avoiding-Robot-with-Timed-Path
An Arduino-powered autonomous robot that follows a timed movement sequence, then intelligently avoids obstacles using an ultrasonic sensor and servo-controlled scanning.

---

## Features
- Autonomous navigation using ultrasonic sensor (HC-SR04)
- 180° environment scanning with servo motor
- Obstacle detection and avoidance using directional decision-making
- Initial timed movement sequence (forward, backward, alternating turns)
- Controlled by Arduino Uno and dual L293D motor drivers

---

## Components Used
- Arduino Uno
- HC-SR04 Ultrasonic Sensor
- SG90 Servo Motor
- 4 DC motors
- 2 × L293D Motor Driver ICs
- Breadboard & Jumper Wires
- 2 × 9V Batteries (for motor power)
- USB cable (for Arduino power)

---

## Circuit Diagram
![Circuit](<img width="1280" height="730" alt="image" src="https://github.com/user-attachments/assets/28740d1c-b444-428f-8557-2f83e7a5ee1c" />
)


---

## How It Works

1. **Timed Movements**:
   - Moves forward for 30 seconds.
   - Moves backward for 1 minute.
   - Alternates turning left/right for 1 minute.

2. **Obstacle Avoidance Mode**:
   - Continuously scans the front using ultrasonic sensor.
   - If an object is detected within ~55 cm:
     - Stops, reverses, then scans right and left.
     - Turns in the direction with more open space.
   - Repeats infinitely.

---

## Code Overview

- `forward()`, `back()`, `turnleft()`, `turnright()`: Motor control functions.
- `Stop()`: Stops all motors.
- `ping()`: Triggers ultrasonic distance check.
- `rightD()` & `leftD()`: Servo turns sensor and measures distance on each side.
- Main loop:
  - Runs the timed routine once.
  - Enters continuous smart navigation afterward.

---

## Tinkercad Simulation  
Try it online:  
[View Project on Tinkercad](https://www.tinkercad.com/things/7L4jgHJg0Er/editel?returnTo=%2Fdashboard)


---

## Author: Eman Alnahdi.

