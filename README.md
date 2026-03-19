# 🐄 Smart Livestock Management System

![IoT](https://img.shields.io/badge/Domain-IoT-green)
![ESP32](https://img.shields.io/badge/Microcontroller-ESP32-blue)
![Communication](https://img.shields.io/badge/Communication-ESP--NOW%20%2F%20LoRa-orange)
![Status](https://img.shields.io/badge/Project-Prototype-yellow)

**An IoT-based smart livestock monitoring system that tracks animal health, location, and environmental conditions in real-time.**

---

## 📌 Project Overview

This project focuses on improving livestock management using **embedded systems and wireless communication**.

Each animal is equipped with a **sensor node (ESP32-based)** that continuously monitors:

- Body temperature  
- Location (GPS)  
- Activity / movement  
- Environmental conditions  

The collected data is transmitted wirelessly to a **base station**, which uploads it to a **cloud database (Firebase)** for real-time monitoring.

This enables farmers to:
- Detect health issues early  
- Track animal movement  
- Reduce manual monitoring effort  

---

## 🏗 System Architecture
Cow Node (ESP32 + Sensors + GPS) │ │  ESP-NOW / LoRa Communication ▼ Base Station (ESP32) │ ▼ Cloud (Firebase) │ ▼ Dashboard / Mobile View

---

## ⚙️ Hardware Components

- ESP32 DevKit (Node + Base Station)  
- GPS Module (Neo-6M or similar)  
- Temperature Sensor (DHT22 / DS18B20)  
- Motion Sensor (optional - accelerometer)  
- LoRa Module (RA-02) *(optional for long range)*  
- Power Supply / Battery  
- Jumper wires & enclosure  

---

## 📡 Communication Methods

### 🔹 ESP-NOW (Recommended for Prototype)
- Direct ESP32 ↔ ESP32 communication  
- Low latency  
- No internet required  
- Range: ~200–300 meters  

### 🔹 LoRa (For Real Deployment)
- Long-range communication (1–5 km)  
b- Suitable for large farms  
- Lower data rate  

---

## 🧠 System Functionality

### 🐄 Animal Node (Transmitter)
- Reads sensor data  
- Fetches GPS coordinates  
- Sends structured data:ID, LAT, LON, TEMP, ACTIVITY

- ---

### 🖥 Base Station (Receiver)
- Receives data from nodes  
- Parses incoming packets  
- Sends data to Firebase  

---

### ☁️ Cloud & Dashboard
- Real-time monitoring  
- Animal tracking on map  
- Alerts for abnormal conditions  

---

## 🚀 Features

- Real-time livestock monitoring  
- Wireless communication (ESP-NOW / LoRa)  
- GPS-based tracking  
- Health monitoring system  
- Cloud integration (Firebase)  
- Scalable architecture  

---

## 📂 Repository Structure
smart-livestock-system │ ├── transmitter-node │   └── sensor_node.ino │ ├── receiver-base │   └── base_station.ino │ ├── firebase │   └── firebase_config.ino │ ├── dashboard │   └── web_dashboard.html │ ├── images │   └── prototype.jpg │ └── README.md

---

## 📸 Prototype

![Prototype](images/prototype.jpg)

---

## 🔮 Future Improvements

- Machine learning for health prediction  
- Battery optimization for long-term use  
- Geofencing alerts  
- Mobile app integration  
- Multi-node scaling  
- Solar-powered system  

---

## 🎯 Applications

- Smart dairy farms  
- Livestock tracking  
- Veterinary monitoring  
- Precision agriculture  


---

## 👨‍💻 Team

- Pratham Shetty  
- Gowtham N
- Prajwal P
- Dheeraj
- Chandan

---

## ✨ Conclusion

This project demonstrates how **IoT can transform traditional livestock management into a data-driven system**.

By enabling **real-time monitoring, tracking, and alerts**, it improves animal health, reduces losses, and increases farm efficiency.

**“Monitor smarter. Act faster. Farm better.”**
