# AI Smart Home Command Center

A modern, responsive web dashboard for monitoring and controlling IoT devices via MQTT and ThingSpeak.

## Features
- **Live Video Stream:** Real-time ESP32-CAM integration.
- **Bi-directional Control:** Toggle Fans and LEDs with active-low relay logic.
- **Environmental Monitoring:** Real-time Air Quality (MQ series) and Rain sensor tracking.
- **Data Analytics:** Historical charts powered by ThingSpeak.
- **Responsive Design:** Dark mode UI that works on Mobile, Tablet, and Desktop.

## Setup
1. **MQTT Broker:** Uses EMQX Public Broker (`wss://broker.emqx.io:8084/mqtt`).
2. **Hardware:** Designed for ESP32/ESP8266.
3. **Configuration:** - Open `index.html`.
   - Update the `CONFIG` object in the `<script>` tag with your ThingSpeak Channel ID.
   - Update the `<img>` src with your local ESP32-CAM IP address.

## MQTT Topics
| Topic | Description |
|-------|-------------|
| `home/sensor/gas` | Air quality ppm values |
| `home/sensor/rain` | 1 for Rain, 0 for Clear |
| `home/fan` | Fan control (Relay sync) |
| `home/led` | LED control |
