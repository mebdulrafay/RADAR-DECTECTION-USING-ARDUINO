<div align="center">

<!-- HERO BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a1628,50:0d4f3c,100:00c896&height=200&section=header&text=📡%20RADAR%20DETECTION&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=AI%20Voice%20Radar%20System%20•%20Arduino%20%2B%20Ultrasonic%20%2B%20TTS&descAlignY=58&descSize=16" width="100%"/>

<br/>

<!-- BADGES ROW 1 -->
[![Arduino](https://img.shields.io/badge/Built%20with-Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)](https://www.arduino.cc)
[![AI Voice](https://img.shields.io/badge/Feature-AI%20Voice%20TTS-22c55e?style=for-the-badge&logo=google&logoColor=white)]()
[![Status](https://img.shields.io/badge/Status-Active-00c896?style=for-the-badge&logo=statuspage&logoColor=white)]()
[![License](https://img.shields.io/badge/License-Open%20Source-10b981?style=for-the-badge)](LICENSE)

<!-- BADGES ROW 2 -->
[![GitHub](https://img.shields.io/badge/GitHub-mebdulrafay-181717?style=flat-square&logo=github)](https://github.com/mebdulrafay)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Hafiz%20Abdul%20Rafay-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/hafiz-abdul-rafay-4577a5395/)
[![Email](https://img.shields.io/badge/Email-mebdulrafay@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mebdulrafay@gmail.com)
[![PAEC](https://img.shields.io/badge/🏆%20Award-Science%20Expo%202025%20(2nd%20Place)-f59e0b?style=flat-square)]()

<br/>

> **📡 AI Voice Based Arduino Ultrasonic Radar** — An advanced, interactive radar system that combines hardware precision with AI-powered voice feedback. Built for smart detection, real-time distance measurement, and human-like audio alerts.

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Circuit Connections](#-circuit-connections)
- [Working Principle](#-working-principle)
- [AI Voice Feature](#-ai-voice-feature)
- [How to Run](#-how-to-run)
- [Applications](#-applications)
- [Future Improvements](#-future-improvements)
- [About the Author](#-about-the-author)

---

## 🌐 Overview

**RADAR DETECTION USING ARDUINO** is a production-ready hardware+software project that uses an **HC-SR04 ultrasonic sensor** mounted on a **servo motor** for 180° scanning, paired with an **AI Text-to-Speech system** to deliver real-time voice alerts — a significant step beyond the typical buzzer-based approach.

```
Servo Rotates (0° → 180°)  ──►  Ultrasonic Pulse  ──►  Object Detected?
                                                               │
                          ┌────────────────────────────────────┤
                          ▼                                    ▼
                  Distance Calculated                   No Object Found
                  via Echo Timing                       (Continue Scan)
                          │
                          ▼
                  Serial Communication
                  (Arduino → PC/Mobile)
                          │
                          ▼
                  AI TTS Voice Alert
             "Distance is 30 centimeters"
```

### ✨ What Makes This Special

- 📡 Full **180° sweep** radar scanning
- 🔊 **AI Voice (TTS)** alerts — human-like speech instead of buzzers
- 📏 Precise **distance measurement** in centimeters
- 🖥️ Optional **Processing visualization** for live radar display
- 🧩 **Beginner-to-intermediate** level — clean, well-documented code

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                   RADAR SYSTEM ARCHITECTURE                          │
├─────────────────────────────────────────────────────────────────────┤
│                                                                       │
│   ┌────────────────────┐      ┌──────────────────────────────────┐  │
│   │   Servo Motor      │─────►│       Arduino Uno (Brain)         │  │
│   │  (SG90 • Pin D9)   │      │  Reads distance, controls sweep   │  │
│   └────────────────────┘      └───────────┬──────────────────────┘  │
│                                           │                           │
│                    ┌──────────────────────┼──────────────────────┐   │
│                    │                      │                       │   │
│             HC-SR04 Sensor          Serial (USB)            Distance  │
│                    │                      │                   Data    │
│          ┌─────────▼──────┐   ┌──────────▼──────┐              │    │
│          │  Trig → D10    │   │   PC / Mobile    │              │    │
│          │  Echo → D11    │   │  AI TTS System   │◄─────────────┘    │
│          └────────────────┘   └─────────┬───────┘                    │
│                                         │                             │
│                              ┌──────────▼────────────┐               │
│                              │    AI VOICE OUTPUT    │               │
│                              ├───────────────────────┤               │
│                              │ 🔊 "Object detected"  │               │
│                              │ 📏 "Distance is X cm" │               │
│                              │ ⚠️  "Warning! Too close"│              │
│                              └───────────────────────┘               │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 🛠 Tech Stack

### ⚙️ Hardware Components

| Component | Model | Role |
|:---:|:---|:---:|
| ![Arduino](https://img.shields.io/badge/Arduino-Uno-00979D?style=flat-square&logo=arduino&logoColor=white) | Arduino Uno | Main microcontroller |
| ![Sensor](https://img.shields.io/badge/Sensor-HC--SR04-10b981?style=flat-square) | HC-SR04 Ultrasonic | Object detection & distance |
| ![Servo](https://img.shields.io/badge/Servo-SG90-22c55e?style=flat-square) | SG90 Servo Motor | 180° rotational sweep |
| ![Misc](https://img.shields.io/badge/Misc-Breadboard%20%2B%20Wires-6b7280?style=flat-square) | Breadboard + Jumper Wires | Circuit assembly |
| ![USB](https://img.shields.io/badge/Interface-USB%20Cable-4b5563?style=flat-square) | USB Cable | Serial communication |

### 💻 Software & Tools

| Tool | Purpose | Type |
|:---:|:---|:---:|
| ![Arduino IDE](https://img.shields.io/badge/Arduino_IDE-Firmware-00979D?style=flat-square&logo=arduino&logoColor=white) | Upload code to Arduino | `Firmware` |
| ![Python](https://img.shields.io/badge/Python-AI_Voice_TTS-3776AB?style=flat-square&logo=python&logoColor=white) | Text-to-Speech voice alerts | `AI Layer` |
| ![Processing](https://img.shields.io/badge/Processing-Radar_Visualizer-006699?style=flat-square) | Optional radar sweep animation | `Visualization` |
| ![Serial](https://img.shields.io/badge/Serial_Comm-USB_Bridge-f59e0b?style=flat-square) | Arduino ↔ PC data stream | `Interface` |

---

## 🔌 Circuit Connections

### Ultrasonic Sensor (HC-SR04)

| Sensor Pin | Arduino Pin |
|:---:|:---:|
| VCC | 5V |
| GND | GND |
| Trig | **D10** |
| Echo | **D11** |

### Servo Motor (SG90)

| Wire Color | Arduino Pin |
|:---:|:---:|
| 🔴 Red | 5V |
| ⚫ Brown / Black | GND |
| 🟡 Yellow (Signal) | **D9** |

---

## ⚙️ Working Principle

```
Step 1 ──► Servo motor sweeps ultrasonic sensor from 0° to 180°
Step 2 ──► HC-SR04 emits ultrasonic sound pulses at each angle
Step 3 ──► Sound waves bounce back after hitting an object
Step 4 ──► Arduino measures echo time → calculates distance (cm)
Step 5 ──► Distance data sent to PC via Serial USB connection
Step 6 ──► AI TTS system converts data into human voice alerts
Step 7 ──► User receives real-time spoken feedback
```

---

## 🔊 AI Voice Feature

<table>
<tr>
<td width="50%">

### 🤖 How It Works
- Object presence is announced in real-time
- Distance is spoken aloud in centimeters
- Close-range warnings trigger urgent alerts
- No buzzer — pure AI-generated voice output
- Compatible with Python, Web, or Mobile TTS engines

</td>
<td width="50%">

### 🔈 Example Voice Messages
- ✅ *"Object detected"*
- 📏 *"Distance is 30 centimeters"*
- ⚠️ *"Warning! Object very close"*
- 🔕 *"No object detected"*
- 🔄 *"Scanning..."*

</td>
</tr>
</table>

---

## ▶️ How to Run

**1. Assemble the hardware**
```
Connect HC-SR04 and SG90 Servo as per the circuit diagram above.
```

**2. Upload Arduino firmware**
```
Open Arduino IDE → Load Arduino Code → Select Board: Arduino Uno → Upload
```

**3. Connect Arduino to PC**
```
Use USB cable → Note the COM port (e.g., COM3 or /dev/ttyUSB0)
```

**4. Run the AI voice system**
```bash
# Python TTS example
pip install pyttsx3 pyserial
python ai_voice.py
```

**5. (Optional) Launch radar visualizer**
```
Open Processing IDE → Load Processing Code → Run sketch
```

**6. Test it**
```
Place your hand in front of the sensor and listen to the AI voice alerts!
```

---

## 📌 Applications

| Use Case | Description |
|:---|:---|
| 🔐 Smart Security | Detect intruders with voice-based alerts |
| 🤖 Robotics | Obstacle avoidance for autonomous bots |
| ♿ Assistive Technology | Distance aid for visually impaired users |
| 🎓 AI + Arduino Learning | Educational project combining hardware and AI |
| 🚗 Reverse Parking Aid | Car proximity detection system prototype |

---

## 🧠 Future Improvements

- 🌐 AI voice support in **Urdu & English**
- 📊 Enhanced **radar animation** with Processing
- 📶 **Wireless** alerts via Bluetooth / WiFi
- 📷 **Camera-based** object identification
- 📱 **Mobile app** integration for remote monitoring

---

## 👨‍💻 About the Author

<div align="center">

| Field | Detail |
|:---:|:---|
| **Name** | Hafiz Abdul Rafay |
| **Role** | Student • AI-Assisted Developer • Freelancer |
| **Location** | 📍 Mianwali, Pakistan |
| **Achievement** | 🏆 2nd Place — Science Expo 2025, PAEC Education Center (Level VI–VIII) |
| **Certification** | 🎓 HP LIFE Certified — AI's Business Impact & Ethics |

</div>

### 🤝 Connect with Abdul Rafay

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-mebdulrafay-181717?style=for-the-badge&logo=github)](https://github.com/mebdulrafay)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/hafiz-abdul-rafay-4577a5395/)
[![Email](https://img.shields.io/badge/Email-Say%20Hello!-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mebdulrafay@gmail.com)

</div>

---

### 📌 Full Project Portfolio

| Project | Stack | Description |
|:---|:---|:---|
| 📡 **Radar System** | Arduino • Ultrasonic • TTS | *This project* — Object detection with AI voice alerts |
| 🌦 **Weather Forecast App** | HTML/CSS/JS • OpenWeather API | Responsive live weather app with dynamic UI |
| 🔢 **Binary Converter** | Python • PyQt5 | Desktop app for efficient text-to-binary conversion |
| 🔔 **PC-Controlled Buzzer** | Arduino • Serial Comm | Hardware alert system controlled via PC |
| 🌐 **Personal Portfolio** | HTML/CSS/JS • Glassmorphism | Premium interactive site showcasing all projects |
| 🤖 **ROEX AI Assistant** | n8n • Gemini • LangChain | AI-powered portfolio representative agent |

---

### 💼 Freelancing Services

| Service | Description |
|:---|:---|
| ⚡ Arduino & IoT Prototyping | Sensor integration, serial comms, and hardware builds |
| 🌐 Modern Web Development | Responsive & premium UI/UX with glassmorphism aesthetics |
| 🤖 AI-Assisted Development | Faster turnaround using AI-powered workflows |
| 🎨 Graphic Design & Branding | Social media creatives, logos, and visual identity |

> 📬 Interested in working together? Reach out at **mebdulrafay@gmail.com**

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c896,50:0d4f3c,100:0a1628&height=100&section=footer" width="100%"/>

**Made with 💚 by [Hafiz Abdul Rafay](https://github.com/mebdulrafay) — Mianwali, Pakistan**

*"Bridging hardware and intelligence — one project at a time."*

⭐ **Star this repo if the radar impressed you!**

</div>
