# Smart Bin Monitoring System

This project implements a smart waste bin monitoring system that provides real-time information about the fill level of a bin. By using an ultrasonic sensor, a microcontroller (Arduino),the system sends data to a visual dashboard built with Node-RED.
This allows for efficient waste management by enabling timely collection only when bins are nearing full, potentially reducing costs and improving urban cleanliness in areas like Nairobi, Kenya.

## Features

* **Real-time Fill Level Monitoring:** Utilizes an ultrasonic sensor to continuously measure the distance to the waste inside the bin, providing an estimate of the fill level.
* **Data Visualization:** Node-RED is used to create an intuitive dashboard displaying the current fill level, historical data, and trends.
* **Near-Full Notifications (Optional):** The system can be configured in Node-RED to send alerts (e.g., email) when a bin reaches a predefined near-full threshold.
* **Configurable Thresholds:** The near-full threshold can be easily adjusted within the Node-RED flow.
* **Local Network Operation:** The current setup operates within a local Wi-Fi network, making it suitable for localized deployments.

## Hardware Components

* **Microcontroller:** Arduino Uno (or similar)
* **Ultrasonic Sensor:** HC-SR04
* **Jumper Wires:** For connecting the components.
* **Power Supply:** For the Arduino and ESP8266.
* **Servo Motor:** For automated lid control (if implemented).

## Software Components

* **Arduino IDE:** Used to program the Arduino microcontroller (written in C/C++).
* **ESP8266 Arduino Core:** Enables programming the ESP8266 using the Arduino IDE.
* **Node-RED:** A flow-based programming tool for IoT, used for data processing, dashboard creation, and notifications.
* **MQTT Broker (Optional):** For more robust and scalable communication between the ESP8266 and Node-RED.
* **Libraries:**
    * `NewPing` library for easier HC-SR04 sensor readings in Arduino.
    * Node-RED nodes: `node-red-dashboard`, `node-red-contrib-mqtt` (if used), notification nodes (e.g., `node-red-node-email`, `node-red-contrib-telegrambot`).

## Wiring Diagram 
![image](https://github.com/user-attachments/assets/7f77f741-c35e-47f7-97d9-22f2bc35e2ff)

## Usage

1.  Power up the Arduino and ESP8266. The ESP8266 should connect to your Wi-Fi network.
2.  The Arduino will start reading data from the ultrasonic sensor and send it to Node-RED (either directly via HTTP requests or via MQTT).
3.  Open your Node-RED dashboard in a web browser (usually at `http://your_node_red_ip:1880/ui`).
4.  You should see the real-time fill level of the bin displayed on the dashboard.


