# 🌡️ Smart Room Temperature Control System

Arduino Uno-based system that monitors room temperature via a DHT22 sensor and automatically triggers a cooling fan, buzzer, and LED alerts when a user-set threshold is exceeded. Built with Embedded C, featuring an I2C LCD display and non-blocking real-time firmware.


---

## 📖 Overview

The Smart Room Temperature Control System is designed to monitor ambient temperature in real time and automatically respond when the temperature exceeds a user-defined threshold.

Using an Arduino UNO and a DHT22 temperature sensor, the system continuously measures room temperature and compares it with the desired set temperature configured by the user through push buttons.

When overheating occurs, the system automatically:
- Activates a cooling fan
- Triggers visual warning indicators
- Sounds an audible alarm
- Displays warning messages on the LCD

The project demonstrates embedded system integration between sensors, actuators, user interfaces, and real-time control logic.

---

# ✨ Features

- 🌡️ Real-time temperature monitoring
- 🎛️ Adjustable set temperature using push buttons
- 🌀 Automatic cooling fan control
- 🔴 Red LED overheating indication
- 🟢 Green LED normal-state indication
- 🔔 Buzzer warning system
- 📟 16×2 I2C LCD live status display
- ⚡ Non-blocking programming using `millis()`
- 🔄 Automatic recovery after cooling
- 🧠 Smart display priority handling

---

# 🛠️ Hardware Components

| Component | Quantity |
|---|---|
| Arduino UNO | 1 |
| DHT22 Sensor | 1 |
| 16×2 I2C LCD | 1 |
| Push Buttons | 2 |
| DC Fan | 1 |
| BC547 Transistor | 1 |
| Red LED | 1 |
| Green LED | 1 |
| Buzzer | 1 |
| Resistors | Multiple |

---

# ⚙️ System Workflow

```text
Read Temperature → Compare with Set Temperature → Trigger Outputs
```

### If Temperature > Set Temperature
- Turn ON Fan
- Flash Red LED
- Activate Buzzer
- Display "Warning: HOT"

### If Temperature Returns to Normal
- Turn OFF Alarm
- Turn OFF Fan
- Turn ON Green LED
- Display Neutral Status

---

# 💻 Software Design

The project was developed using the Arduino IDE with a modular and scalable software architecture.

## Main Functionalities

- Temperature sensing
- User input handling
- LCD display management
- Alarm logic
- Fan control
- Real-time monitoring

## Programming Concepts Used

- Embedded C / Arduino C++
- Digital I/O interfacing
- I2C communication
- Non-blocking timing (`millis()`)
- Real-time control systems

---

# 🚀 Getting Started

## Requirements

- Arduino IDE
- DHT Sensor Library
- LiquidCrystal_I2C Library

## Installation

1. Clone the repository

```bash
git clone https://github.com/your-username/smart-room-temperature-control.git
```

2. Open the project in Arduino IDE

3. Install required libraries:
- DHT Sensor Library
- LiquidCrystal_I2C

4. Connect hardware components

5. Upload the code to Arduino UNO

---

# 🔌 Circuit Diagram

Add your circuit diagram or Tinkercad schematic here.

```md
![Circuit Diagram](<img width="615" height="372" alt="image" src="https://github.com/user-attachments/assets/7f87bf97-9a4a-4f1d-bf19-cb02d4fdae1e" />
)
```

---

# 📷 Project Preview

Add project images here.

```md
![Prototype](<img width="290" height="247" alt="image" src="https://github.com/user-attachments/assets/83f981ad-f688-4143-9b29-256d5adaa1d4" />
)
```

```md
![Simulation](<img width="512" height="292" alt="image" src="https://github.com/user-attachments/assets/51cee28c-9c33-4101-9348-fbb6cb8feadc" />
)
```

---

# 📊 Testing & Results

The system was tested under multiple operating conditions to ensure stable and reliable performance.

## Tested Features

- LCD initialization
- Sensor reading accuracy
- Push button responsiveness
- Fan activation
- Alarm triggering
- Automatic recovery

## Result

The system operated successfully with smooth and responsive behavior during all test scenarios.

---

# 🚧 Challenges & Solutions

## Problem: Slow response caused by `delay()`

### Solution
Implemented non-blocking timing using `millis()` to improve responsiveness.

---

## Problem: Arduino couldn't drive the fan directly

### Solution
Used a BC547 transistor as a switching device for safe fan operation.

---

## Problem: Sensor response limitations

### Solution
Optimized software logic for stable and reliable readings.

---

# 🔮 Future Improvements

- PWM fan speed control
- EEPROM temperature saving
- Bluetooth / Wi-Fi connectivity
- Mobile application integration
- Battery-powered operation
- Smart home integration
- Protective enclosure design

---

# 📂 Project Structure

```text
Smart-Room-Temperature-Control/
│
├── code/
│   └── smart_room_temp_control.ino
│
├── images/
│   ├── circuit.png
│   ├── prototype.jpg
│   └── simulation.png
│
├── report/
│   └── project_report.pdf
│
└── README.md
```

---

# 🧑‍💻 Team Members

- Youssef Salah Elfouly
- Malik Fathi
- Clara Maged

---

# 👨‍🏫 Supervisor

Dr. Samar Moustafa

---

# 📚 References

- Arduino Official Documentation
- DHT22 Datasheet
- LiquidCrystal_I2C Library
- SimulIDE Documentation

---

# 🏷️ Technologies Used

`Arduino` `Embedded Systems` `C++` `DHT22` `LCD I2C` `Electronics` `Automation`

---

# ⭐ Conclusion

This project successfully demonstrates a complete embedded temperature monitoring and control solution using Arduino. The system integrates sensing, processing, automation, and user interaction into a reliable smart environment application while providing practical experience in embedded systems and hardware-software integration.
