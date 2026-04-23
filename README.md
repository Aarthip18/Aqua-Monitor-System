# Aqua-Monitor-System
This Arduino-based Aquaculture Monitoring System provides real-time tracking of water quality. It measures Temperature, pH, Dissolved Oxygen, and Turbidity using analog and 1-Wire sensors. Data is broadcasted via USB and SoftwareSerial for Bluetooth/LoRa integration, ensuring optimal conditions for aquatic life through precise environment tracking.
Since you've provided the code for an **Aquaculture Monitoring System**, I’ve generated a tailored `README.md` that explains exactly what this code does, how to wire the sensors, and how to calibrate it.

# 🐟 Aquaculture Monitoring System

A real-time water quality monitoring solution using Arduino. This system tracks critical environmental parameters to ensure optimal conditions for aquatic life. It reads data from multiple sensors and outputs the results via USB Serial and an auxiliary Serial port (e.g., for Bluetooth or LoRa modules).

## Features

  - **Multi-Sensor Integration**: Simultaneous monitoring of four key water metrics.
  - **Dual Serial Output**: Debugging via USB Serial and data transmission via SoftwareSerial.
  - **Submersible Temp Sensing**: Uses the DS18B20 1-Wire protocol for accurate water temperature.
  - **Expandable**: Calibration offsets built-in for fine-tuning sensor accuracy.

## Monitored Parameters
| Parameter | Sensor Type | Unit | Pin |
| :--- | :--- | :--- | :--- |
| **Temperature** | DS18B20 (Digital) | °C | Digital 2 |
| **Dissolved Oxygen** | Analog Probe | mg/L | Analog 0 |
| **pH Level** | Analog Probe | pH | Analog 1 |
| **Turbidity** | Analog Optical | NTU | Analog 2 |
## Hardware Requirements

  * **Microcontroller**: Arduino Uno, Nano, or Mega.
  * **Sensors**:
      * DS18B20 Waterproof Temperature Sensor.
      * Analog Dissolved Oxygen (DO) Kit.
      * Analog pH Sensor Kit.
      * Analog Turbidity Sensor.
  * **Other**: 4.7k Ohm resistor (for DS18B20 pull-up), Bluetooth Module (HC-05/06) optional.

## Getting Started

### 1\. Library Installation

You will need the following libraries installed in your Arduino IDE:

  - `OneWire`
  - `DallasTemperature`
  - `SoftwareSerial` (Built-in)

### 2\. Wiring

  - **DS18B20**: Connect VCC to 5V, GND to GND, and Data to D2. *Note: Place a 4.7k resistor between VCC and Data.*
  - **Analog Sensors**: Connect VCC to 5V, GND to GND, and Signal pins to A0, A1, and A2 respectively.
  - **Communication**: Connect your external serial device to pins 10 (RX) and 11 (TX).

### 3\. Calibration

For accurate results, you must calibrate your sensors:

1.  Update `PH_CALIBRATION_OFFSET` based on a pH 7.0 buffer solution.
2.  Update `DO_CALIBRATION_OFFSET` based on atmospheric oxygen saturation or a zero-oxygen solution.

-----

## 📖 Data Format

The system outputs a CSV-style string every 5 seconds via SoftwareSerial:
`T:25.50,DO:7.20,pH:7.40,TURB:12`

Contact:
Your Name - mp.aarthi@outlook.in
Project Link: [https://github.com/Aarthip18/Aqua-Monitor-System]

