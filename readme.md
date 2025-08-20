# OLED Speedometer

An Arduino-based GPS speedometer with OLED display that shows real-time speed, location, satellite information, and direction.

## Features

- Real-time speed display (0-200 km/h) with analog-style gauge
- GPS coordinates display
- Satellite count and signal strength indicator
- Direction (cardinal) display
- Local time display with timezone adjustment

## Hardware Requirements

- Arduino Board (Nano recommended)
- NEO-6M or similar GPS module
- SSD1306 128x64 OLED Display
- Connecting wires

## Wiring

| GPS Module | Arduino |
|------------|---------|
| RX         | D3      |
| TX         | D4      |
| VCC        | 3.3V    |
| GND        | GND     |

| OLED Display | Arduino |
|--------------|---------|
| SDA          | A4      |
| SCL          | A5      |
| VCC          | 3.3V    |
| GND          | GND     |

## Libraries Required

- U8glib (for OLED display)
- TinyGPS++ (for GPS data parsing)
- SoftwareSerial (for GPS communication)

## Installation

1. Clone or download this repository
2. Open `OLED_Speedometer.ino` in Arduino IDE
3. Install required libraries
4. Connect hardware as per wiring diagram
5. Upload to Arduino board
6. Wait for GPS signal acquisition

## Configuration

Adjust the timezone in the code:
```cpp
const int timezone_hours = 3; // Change according to your timezone
const int timezone_minutes = 0;