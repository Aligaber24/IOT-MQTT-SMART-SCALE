# IoT Smart Scale with MQTT

This project demonstrates an IoT-based weighing scale that measures weight using a load cell and sends the data over Wi-Fi using MQTT protocol. A Python client subscribes to the MQTT topic to receive and display the weight data in real-time.

## 📦 Project Overview

- **Sensor:** 5kg Load Cell + HX711 module
- **Microcontroller:** ESP8266 or ESP32
- **Communication:** MQTT over Wi-Fi
- **Receiver:** Python script running as an MQTT subscriber

## 🔁 How It Works

1. The ESP reads analog weight values from the HX711 module.
2. It connects to a Wi-Fi network and publishes the weight to a specific MQTT topic.
3. A Python script subscribes to that topic and prints/logs the data.
4. Optionally, the data can be visualized or pushed to a web interface.

## ⚙️ Hardware Used

- ESP8266 (e.g., NodeMCU)
- HX711 load cell amplifier
- 5kg Load Cell
- Breadboard + jumper wires
- Micro USB cable

## 🧠 Software Used

- Arduino IDE for ESP programming
- Python 3.x
- MQTT Broker (e.g., [Mosquitto](https://mosquitto.org/), or [broker.hivemq.com](https://www.hivemq.com/public-mqtt-broker/))
- `paho-mqtt` Python library

## 🚀 Getting Started

### ESP Side

1. Flash the ESP code in `ESP_Code/smart_scale.ino`
2. Update your Wi-Fi credentials and MQTT broker address
3. Connect the circuit (see wiring diagram)
4. Upload code and monitor via Serial

### Python Side

1. Install dependencies:
   ```bash
   pip install paho-mqtt
