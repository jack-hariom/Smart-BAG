# Smart Bag with ESP32 - Multi-Sensor IoT Tracker

## Project Overview
This ESP32-based smart bag integrates multiple sensors to provide:
- GPS location tracking using a UART GPS module
- Heart rate and body temperature monitoring with MAX30105 sensor
- RFID tag scanning for user authentication
- Real-time communication with Adafruit IO via MQTT for remote monitoring and control
- Buzzer alert control from Adafruit IO dashboard commands

## Hardware Components
- ESP32 Dev Module  
- Ublox NEO-6M GPS (UART1 RX=GPIO16, TX=GPIO17)  
- MFRC522 RFID reader (UART2 RX=GPIO4)  
- MAX30105 Heart Rate sensor (I2C)  
- Buzzer (GPIO23)  
- Lithium-ion battery power source with BMS  

## Software Features
- WiFi and MQTT connectivity with Adafruit IO  
- Continuous RFID scanning with access status publishing  
- GPS data parsing and 2-min interval publishing  
- Heart rate reading with optional simulation mode  
- Temperature monitoring and publishing  
- Remote buzzer control via MQTT subscription  

## Usage Instructions
1. Open the single Arduino sketch file.  
2. Update your WiFi SSID, password, Adafruit IO username, and key inside the code before uploading.  
3. Connect the hardware as per pin mapping in the code.  
4. Upload the code to your ESP32.  
5. Open Serial Monitor (baud rate 115200) to view debug messages.  
6. Monitor data and control buzzer via Adafruit IO dashboard.  

## Important Security Notice
- For public sharing, remove or exclude your WiFi and Adafruit IO credentials before uploading.  
- Consider replacing credentials with placeholders before committing.  
- Use a separate config mechanism or environment variables for safer credential management in production.  

## License
This project is open-source under the MIT License.  

## Acknowledgments
- Adafruit MQTT and sensor libraries  
- TinyGPSPlus for GPS parsing  
- Arduino and ESP32 communities  
