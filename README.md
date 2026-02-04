# ESP32-Based Smart Industrial / Home Safety Monitoring System

## Overview
This project is a Smart Industrial/Home Safety Monitoring System developed as part of the
**Analogue and Mixed-Signal Design (5FTC2135)** module.
The system integrates multiple analogue and digital sensors with an ESP32 microcontroller
to detect common safety hazards and provide real-time alerts.

It demonstrates a true **mixed-signal embedded system**, combining analogue signal
conditioning, ADC processing, and digital decision logic in a single platform.

## Objectives
- Detect multiple safety hazards using a single embedded system
- Implement mixed-signal design principles (analogue + digital)
- Provide real-time visual and audible alerts
- Design a low-cost, modular, and energy-efficient safety device

## System Features
- Metal proximity detection
- Door / window intrusion detection
- Water leakage / level monitoring
- Temperature monitoring
- Loud sound detection (analogue processing)
- Manual panic / emergency trigger
- Real-time system status display

## Sensors & Inputs
- **SN04N Inductive Proximity Sensor** – metal detection (digital, level shifted)
- **Magnetic Reed Switch** – door/window intrusion (digital)
- **Float Switch** – water leakage or level detection (digital)
- **DS18B20 Temperature Sensor** – digital temperature monitoring (1-Wire)
- **TTP223 Touch Sensor** – panic / manual alert input
- **SY-M213 Sound Sensor** – analogue sound detection

## Analogue Signal Processing
- Sound sensor signal amplified using **LM358 operational amplifier**
- RC filtering used to reduce noise and unwanted frequencies
- ESP32 ADC samples the conditioned analogue signal
- Software averaging and threshold logic used to avoid false triggers

## Outputs & User Interface
- **1.3” OLED Display (SH1106, I²C)**  
  - SAFE view  
  - STATUS view  
  - ALERT view (flashing)
- **RGB LED**
  - Green → Safe state
  - Red → Hazard detected
- **Buzzer**
  - Audible alerts during hazardous conditions

## Power System
- 12 V DC adapter as main supply
- Buck converter (12 V → 5 V)
- ESP32 onboard regulator (5 V → 3.3 V)
- Decoupling capacitors used for noise suppression
- Designed for stable mixed-signal operation

## Software & Tools
- Arduino IDE (ESP32 board package)
- Adafruit GFX & SH1106 OLED libraries
- OneWire & DallasTemperature libraries
- Wokwi (simulation)
- Proteus / EasyEDA (design & validation)

## Key Engineering Concepts Demonstrated
- Mixed-signal system design
- Analogue signal conditioning
- ADC sampling and averaging
- Digital sensor interfacing
- Embedded state machines
- Real-time alert handling
- Low-power embedded design

## My Contribution
- Sensor wiring and interfacing
- ESP32 firmware development
- Analogue sound detection logic
- Hardware testing and debugging
- System integration and validation
- Technical documentation

## Results
- Successfully detected all defined hazard conditions
- Stable real-time operation with minimal false triggers
- Clear user feedback via display, LED, and buzzer
- Operates continuously with low power consumption

## Future Improvements
- Add Wi-Fi / IoT cloud monitoring
- Mobile app integration
- Data logging and event history
- Additional industrial-grade sensors

## Project Status
Completed

