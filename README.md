# Smart Street Lighting System using ESP32, BH1750, and HC-SR04

## Overview

This project implements an intelligent street lighting system using an ESP32, BH1750 Light Sensor, and HC-SR04 Ultrasonic Sensor. The system automatically controls an LED street light based on ambient light intensity and vehicle/object detection.

The LED turns ON when it is dark and an object is detected within a specified distance. This helps reduce energy consumption while ensuring adequate illumination when needed.

## Features

* Automatic street light control
* Ambient light monitoring using BH1750
* Vehicle/object detection using HC-SR04
* Energy-efficient operation
* Real-time monitoring through Serial Monitor
* ESP32-based implementation

## Components Required

* ESP32 Development Board
* BH1750 Light Sensor
* HC-SR04 Ultrasonic Sensor
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires

## Pin Connections

### BH1750 Sensor

| BH1750 | ESP32   |
| ------ | ------- |
| VCC    | 3.3V    |
| GND    | GND     |
| SDA    | GPIO 21 |
| SCL    | GPIO 22 |

### HC-SR04 Sensor

| HC-SR04 | ESP32   |
| ------- | ------- |
| VCC     | 5V      |
| GND     | GND     |
| TRIG    | GPIO 5  |
| ECHO    | GPIO 18 |

### LED

| LED         | ESP32                  |
| ----------- | ---------------------- |
| Anode (+)   | GPIO 23                |
| Cathode (-) | GND (through resistor) |

## Working Principle

1. The BH1750 continuously measures ambient light intensity in lux.
2. The HC-SR04 detects the distance of nearby objects.
3. If the environment is dark (Lux < 50), the system checks for object detection.
4. If an object is detected within 100 cm, the LED turns ON.
5. If the environment is bright, the LED remains OFF regardless of object detection.
6. The sensor values and LED status are displayed on the Serial Monitor.

## Control Logic

### LED ON

Condition:

```text
Lux < 50
AND
Distance < 100 cm
```

Result:

```text
LED ON
```

### LED OFF

Condition:

```text
Lux ≥ 50
OR
Distance ≥ 100 cm
```

Result:

```text
LED OFF
```

## Serial Monitor Output

### Vehicle Detected at Night

```text
Lux: 15.00 Distance: 45.00
LED ON
```

### No Vehicle Detected

```text
Lux: 15.00 Distance: 150.00
LED OFF
```

### Daytime Condition

```text
Lux: 350.00 Distance: 40.00
LED OFF
```

## Applications

* Smart Street Lighting
* Highway Lighting Systems
* Parking Area Illumination
* Campus Lighting
* Smart City Projects
* Energy Conservation Systems

## Technologies Used

* ESP32
* BH1750 Light Sensor
* HC-SR04 Ultrasonic Sensor
* Arduino IDE
* Embedded C/C++

## Future Improvements

* PWM Brightness Control
* ThingSpeak Cloud Monitoring
* Blynk Mobile Dashboard
* Solar-Powered Street Lighting
* Vehicle Counting System
* AWS IoT Integration

## Project Level

### Level 1

Ambient light monitoring.

### Level 2

Vehicle detection using ultrasonic sensor.

### Level 3

Intelligent street light automation and energy management.

OUTPUT
https://github.com/PandrangiJahnavi/Smart_street_ligth/blob/main/Screenshot%202026-06-17%20091946.png
https://github.com/PandrangiJahnavi/Smart_street_ligth/blob/main/Screenshot%202026-06-17%20092018.png
https://github.com/PandrangiJahnavi/Smart_street_ligth/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.50.18%20AM%20(1).jpeg
https://github.com/PandrangiJahnavi/Smart_street_ligth/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.50.18%20AM.jpeg
https://github.com/PandrangiJahnavi/Smart_street_ligth/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.51.24%20AM.jpeg

## Author

**Pandrangi Jahnavi**

B.E. Electronics and Communication Engineering (ECE)

IoT | Embedded Systems | Smart City Solutions | Industrial IoT
