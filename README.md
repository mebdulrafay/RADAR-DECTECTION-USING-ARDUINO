# RADAR-DECTECTION-USING-ARDUINO
# 📡🤖 AI Voice Based Arduino Ultrasonic Radar

This project is an **Advanced Radar System** built using **Arduino, Ultrasonic Sensor, Servo Motor**, and an **AI Voice (Text-to-Speech) system**.  
Unlike traditional radar projects, this system provides **real-time AI voice feedback** when an object is detected.

---

## 🚀 Key Features
- 180° radar scanning
- Real-time object detection
- Distance measurement in centimeters
- AI-based voice alerts (human-like speech)
- Interactive and smart radar system
- Beginner to intermediate level project

---

## 🛠 Components Used
- Arduino Uno
- Ultrasonic Sensor (HC-SR04)
- Servo Motor (SG90)
- Breadboard
- Jumper Wires
- USB Cable
- PC / Mobile (for AI Voice – TTS)

---

## 🔊 AI Voice Feature (Main Highlight)

### 🤖 AI Voice Alert System
This project includes an **AI-based Text-to-Speech (TTS) voice system**.

- When an object is detected, the system announces:
  - Object presence
  - Distance from the radar
  - Warning messages for close objects
- Voice alerts are generated using **AI TTS** instead of a buzzer.

### Example AI Voice Messages
- "Object detected"
- "Distance is 30 centimeters"
- "Warning! Object very close"
- "No object detected"

---

## 🔌 Circuit Connections

### Ultrasonic Sensor (HC-SR04)
| Pin | Arduino |
|----|--------|
| VCC | 5V |
| GND | GND |
| Trig | D10 |
| Echo | D11 |

### Servo Motor
| Wire | Arduino |
|-----|--------|
| Red | 5V |
| Brown/Black | GND |
| Yellow | D9 |

---

## ⚙️ Working Principle
1. Servo motor rotates the ultrasonic sensor from **0° to 180°**.
2. Ultrasonic sensor sends sound waves.
3. Waves reflect back after hitting an object.
4. Arduino calculates the distance.
5. Distance data is sent via **Serial Communication**.
6. AI system converts data into **voice alerts**.
7. User hears real-time spoken feedback.

---

## 💻 Software & Tools
- Arduino IDE
- Serial Communication
- AI Text-to-Speech (TTS)
  - Python / Web / Mobile based AI voice
- Optional: Processing for radar visualization

---

## ▶️ How to Run
1. Make all hardware connections.
2. Upload Arduino code using Arduino IDE.
3. Connect Arduino to PC / Mobile.
4. Run AI voice system (TTS).
5. Place an object in front of the sensor.
6. Listen to AI voice alerts.

---

## 📌 Applications
- Smart security systems
- Obstacle detection
- Assistive technology
- Robotics projects
- AI + Arduino learning projects

---

## 🧠 Future Improvements
- AI voice in Urdu & English
- Radar animation using Processing
- Wireless communication (Bluetooth / WiFi)
- Camera-based object detection
- Mobile app integration

---

## 👨‍💻 Author
**HAFIZ ABDUL RAFAY**  
Arduino | AI ASSISTED COODER 

---

## 📄 License
This project is open-source and free to use for educational purposes.

