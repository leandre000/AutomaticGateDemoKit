# 🚧 Automatic Gate Demo Kit – Arduino Project

## 📖 Project Overview

This project demonstrates how an **Arduino Uno** can control an **automated gate** using real-time sensor input. The system uses:

- An **ultrasonic sensor** to detect approaching objects
- A **servo motor** to act as the gate
- **LEDs** for status indication
- A **buzzer** for audible alerts

It mimics a real-world automatic barrier system, ideal for smart parking, building entry control, or learning embedded systems.

---

## 🎯 Objectives

- Detect an object using an **ultrasonic sensor**
- Open a gate automatically using a **servo motor** when the object is near
- Keep the gate open for 5 seconds and then close it
- Indicate gate status with:
  - **Red LED** when gate is **closed**
  - **Blue LED** when gate is **open**
- **Beep the buzzer** continuously when the gate is open

---

## 🧰 Components Used

| Component            | Description                        |
|---------------------|------------------------------------|
| Arduino Uno          | Microcontroller board              |
| HC-SR04              | Ultrasonic distance sensor         |
| Servo motor          | For gate rotation                  |
| Red LED              | Indicates "Gate Closed"            |
| Blue LED             | Indicates "Gate Open"              |
| Buzzer               | Sounds when gate is open           |
| Jumper Wires         | For connections                    |
| Breadboard (optional)| For wiring                         |

---

## ⚙️ Circuit Connections

| Component         | Arduino Pin        |
|------------------|--------------------|
| HC-SR04 Trigger  | Pin 2              |
| HC-SR04 Echo     | Pin 3              |
| Red LED Anode    | Pin 4              |
| Red LED Cathode  | Pin 8 (set LOW)    |
| Blue LED         | Pin 5              |
| Blue LED Cathode | Pin 7 (set LOW)    |
| Servo Motor      | Pin 6              |
| Buzzer           | Pin 12             |

> 🔋 **Note:** Use current-limiting resistors for LEDs (e.g., 220Ω) if needed.

---

## 📦 Code Behavior

### ✅ Startup:
- Servo is at `0°` (closed)
- Red LED is **ON**
- Blue LED and Buzzer are **OFF**

### 🚗 Object Detected (within 50 cm):
- Servo rotates to `90°` (open)
- Blue LED turns **ON**, Red LED turns **OFF**
- Buzzer **beeps briefly**

### ⏳ While Object Stays:
- Gate remains open

### 🕔 After Object Leaves (for 5 seconds):
- Servo returns to `0°` (closed)
- Red LED turns **ON**, Blue LED turns **OFF**
- Buzzer stays **OFF**

---

## 🧠 Key Concepts Demonstrated

- Sensor-based automation
- Servo motor control
- Non-blocking timing logic
- LED indicators & alert systems
- Real-world decision-making using Arduino

---

## 🧪 Sample Output Behavior

