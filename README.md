# 🚀 ESP32 MQTT Smart Button to LED Control (Wokwi + Adafruit IO)

## 📌 Project Name
**ESP32 MQTT Multi-Button Remote LED Control System**

---

## 📖 Description
This project demonstrates an **IoT-based remote control system** using two ESP32 boards.  

- One ESP32 acts as a **Button Controller Node**  
- Another ESP32 acts as an **LED Receiver Node**  

When a button is pressed on the first ESP32, a message is sent using **MQTT protocol** through **Adafruit IO cloud**.  
The second ESP32 receives the message and toggles the corresponding LED.

The system is simulated using **Wokwi IoT Simulator**.

---

## 🎯 Features
✅ 4 Push Button Inputs  
✅ 4 LED Outputs  
✅ MQTT Cloud Communication  
✅ Adafruit IO Integration  
✅ Real-time Device-to-Device Communication  
✅ Wokwi Simulation Support  

---

## 🛠 Technologies Used

### 💻 Software
- Embedded C / Arduino Framework  
- MQTT Protocol  
- Adafruit IO Cloud  
- Wokwi Simulator  

### 📚 Libraries
- WiFi.h  
- PubSubClient.h  

---

## 🔌 Hardware / Simulation Components
- ESP32 DevKit  
- Push Buttons × 4  
- LEDs × 4  
- Resistors (1kΩ) × 4  

---

## 🧠 Working Principle

### 🔘 Button Node
- Reads button press using GPIO pins  
- Sends `"TOGGLE"` message to MQTT feed  

### 💡 LED Node
- Subscribes to MQTT feeds  
- Toggles LED state when message received  

---

## 📡 MQTT Feed Structure
username/feeds/r1
username/feeds/r2
username/feeds/r3
username/feeds/r4


---

## 📂 Project Structure
├── Button_Node_Code
├── LED_Node_Code
├── Wokwi_Button_Circuit.json
├── Wokwi_LED_Circuit.json
└── README.md


---

## ⚙ Setup Instructions

### 1️⃣ Create Adafruit IO Account
- Create account  
- Create feeds: r1, r2, r3, r4  
- Copy Username & AIO Key  

---

### 2️⃣ Update Credentials in Code
#define MQTT_USER "your_username"
#define MQTT_KEY "your_aio_key"


---

### 3️⃣ Run Simulation
Open two Wokwi simulations:
- One → Button Node  
- One → LED Node  

Press button → LED toggles remotely.

---

## 🧪 Testing
✔ Check WiFi connection in Serial Monitor  
✔ Check MQTT connection  
✔ Verify feed messages in Adafruit IO Dashboard  

---

## 🚨 Troubleshooting
❌ LEDs not responding  
➡ Check MQTT username and key  
➡ Verify feeds exist in Adafruit IO  
➡ Ensure both ESP32 devices connected to WiFi  

---

## 🌍 Applications
- Smart Home Automation  
- Remote Switch Control  
- Industrial Monitoring  
- IoT Learning Projects  


## 📜 License
This project is for educational purposes.
