# Smart Bag with ESP32 - Multi-Sensor IoT Tracker

## Project Overview
This ESP32-based smart bag integrates multiple sensors to provide:
- GPS location tracking using UART GPS module
- Heart rate and body temperature monitoring using MAX30105 pulse oximeter sensor
- RFID tag scanning for user authentication
- Real-time communication with Adafruit IO via MQTT for remote monitoring and control
- Buzzer alert control from Adafruit IO dashboard commands

## Hardware Components
- ESP32 Dev Module
- Ublox NEO-6M GPS module (UART1 on GPIO16, 17)
- MFRC522 RFID reader (UART2 RX on GPIO4)
- MAX30105 sensor for heart rate and temperature (I2C)
- Buzzer (GPIO23)
- Lithium-ion battery power source with BMS for safe operation
- 0.96" OLED Display (optional for debug)

## Software Features
- WiFi connectivity and MQTT client for Adafruit IO data exchange
- Continuous RFID scanning for access control with real-time status publishing
- GPS data parsing with location publishing every 2 minutes
- Heart rate reading and optional simulation mode for testing without sensor
- Temperature monitoring and publishing
- Remote buzzer control with MQTT subscription
- Code structured for clarity and modularity

## Getting Started
1. Clone this repository.
2. Create a `config.h` file based on `config_template.h` and add your WiFi and Adafruit IO credentials.
3. Connect the hardware components according to the pinout in the documentation.
4. Open the `src/main.ino` in Arduino IDE or PlatformIO and upload to your ESP32 board.
5. Open Serial Monitor at 115200 baud to observe sensor and connection logs.
6. Access your Adafruit IO dashboard to monitor data and control the buzzer.

## Security Notes
- Do **NOT** commit your `config.h` with real credentials.
- Use `.gitignore` to exclude sensitive files.
- Use secure passwords and API keys.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Adafruit Libraries for MQTT and OLED support
- TinyGPSPlus for GPS data handling
- MAX30105 sensor community projects and example code
- Arduino and ESP32 communities

