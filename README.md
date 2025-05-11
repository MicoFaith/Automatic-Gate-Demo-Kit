# Automatic-Gate-Demo-Kit

🔧 Ultrasonic Sensor Gate System with Servo, LEDs & Buzzer
This Arduino project uses an ultrasonic sensor to detect nearby objects and control a servo motor, LEDs, and a buzzer. When an object is detected within a specified distance, the servo "gate" opens, LEDs indicate the status, and a buzzer produces a "bump-bump" sound effect.

🚀 Features
Object Detection using an HC-SR04 Ultrasonic Sensor

Automated Gate using a Servo Motor (opens when object detected, closes after delay)

Visual Feedback with Red and Blue LEDs

Auditory Feedback with a Buzzer ("bump bump" pattern)

Simple state machine with time-based control

🛠️ Hardware Requirements
Arduino Uno or compatible board

HC-SR04 Ultrasonic Sensor

Servo Motor (e.g., SG90)

Red LED with appropriate resistor

Blue LED with appropriate resistor

Piezo Buzzer

Jumper wires

Breadboard

🗂️ Pin Configuration
Component	Arduino Pin
Ultrasonic Trigger	2
Ultrasonic Echo	3
Red LED Anode	4
Red LED Cathode	8
Blue LED Anode	5
Blue LED Cathode	7
Servo Motor	6
Buzzer	12

⚙️ How It Works
Detection: The ultrasonic sensor continuously checks for objects within a threshold distance (20 cm).

Action:

If detected:

Servo opens the gate (90°).

Blue LED turns on.

Red LED turns off.

Buzzer starts a “bump bump” loop.

If no object is detected for 5 seconds:

Servo closes the gate (0°).

Blue LED turns off.

Red LED turns on.

Buzzer stops.

⏱️ Timing Logic
Gate remains open for 5 seconds after the last object detection.

Buzzer timing:

ON for 100 ms

OFF for 800 ms

🧠 Code Overview
getDistance(): Returns the distance measured by the ultrasonic sensor.

loop(): Handles state transitions for servo, LEDs, and buzzer.

Uses millis() for non-blocking time-based events.

📷 Optional Enhancements
Add an LCD to display distance.

Use a push-button to manually open/close the gate.

Record object detection events with timestamps (using RTC module).

📄 License
This project is open-source and free to use under the MIT License.
