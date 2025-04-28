# ESP32 Earthquake Detector

This project uses an ESP32, MPU6050 accelerometer, buzzer, LED, and ESP-Mail-Client to detect earthquakes and send email alerts.

## Hardware Required
- ESP32 board
- MPU6050 module (Accelerometer + Gyroscope)
- Buzzer
- LED
- 220 ohm resistor (for LED)
- Jumper wires
- Breadboard

## Connections
| ESP32 Pin | MPU6050 Pin |
|:---------:|:-----------:|
| GPIO21 (SDA) | SDA |
| GPIO22 (SCL) | SCL |
| 3.3V | VCC |
| GND | GND |

**Buzzer:** GPIO26  
**LED:** GPIO25

## How It Works
- ESP32 reads vibration data from MPU6050.
- If acceleration exceeds a threshold, it estimates earthquake magnitude.
- Triggers buzzer + LED flashing.
- Sends email alert (if connected to WiFi).

## Notes
- Adjust `EARTHQUAKE_THRESHOLD` if false positives occur.
- Use Gmail App Password (for `AUTHOR_PASSWORD`) if using Gmail.

## Libraries
- `ESP_Mail_Client` (latest version)
- `Wire.h`

## License
Open-source for personal and educational use.