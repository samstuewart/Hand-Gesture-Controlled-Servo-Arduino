# Hand Gesture Controlled Servo System

This project enables real-time control of servo motors through hand gestures. It combines **Python** (MediaPipe for hand tracking) and **Arduino** for servo motor control. Finger positions are tracked using a webcam, mapped to servo angles, and transmitted via serial communication to the Arduino, which drives the motors accordingly.

---

## Features
- Real-time hand gesture detection and tracking.
- Maps finger movements to servo motor angles (0–180°).
- Serial communication for data transfer between Python and Arduino.
- Supports five servos representing thumb, index, middle, ring, and pinky fingers.
- Interactive and responsive control system.

---

## How It Works
1. **Hand Gesture Tracking**:
   - Uses MediaPipe to detect hand landmarks via webcam input.
   - Extracts the positions of finger tips and maps their y-coordinates to servo angles.

2. **Angle Mapping**:
   - Maps the normalized finger tip positions to a range of 0 to 180° for servo control.

3. **Data Transmission**:
   - Transmits mapped servo angles as a comma-separated string from Python to Arduino via serial communication.

4. **Servo Control**:
   - Arduino reads the incoming angles and adjusts the servos to match the positions.

---

## Requirements

### Hardware
- **Arduino Uno/Nano/Mega** (or compatible board)
- **5 Servo Motors**
- **Webcam**
- External power supply for servo motors (optional for higher torque).

### Software
- **Python 3.x**
- **Arduino IDE**

### Python Libraries
Install the required Python libraries:
```bash
pip install opencv-python mediapipe pyserial
