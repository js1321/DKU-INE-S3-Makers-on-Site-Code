# DKU-INE-S3-Makers-on-Site-Code
MicroBlocks project for DKU INE Lab Session 3 smart car prototype.
BLE wireless control system with AI-assisted recognition.

## Project Photos
### Full Prototype
![Smart Car Full Prototype](https://github.com/js1321/DKU-INE-S3-Makers-on-Site-Code/blob/17b2fdac08cc5c53647a2f02259ac20fdbd88998/assests/car_overview.jpg)

### Circuit Diagram
![Circuit Diagram](assets/circuit_diagram.jpg)

### Wiring Connection
![Wiring Connection](assets/wiring_connection.jpg)

## Project Overview
This project builds a wireless smart car system using two ESP32 boards programmed with MicroBlocks.
The system is split into two parts:
1. Transmitter board: Collects sensor data, runs recognition logic, calculates control signals, and sends movement commands through BLE Bluetooth.
2. Receiver (controller) board: Receives BLE commands and drives servo motors to control the car to move forward, backward, turn left and turn right.

## Hardware Components
- 2 × ESP32 microcontroller boards
- Servo motors for motion control
- On-board sensors for the recognition module
- Power supply modules

## Core Functions
1. BLE radio wireless communication between two ESP32 devices
2. Sensor data acquisition and AI-assisted recognition
3. Real-time command transmission
4. Servo motor control: forward, back, left turn, right turn

## Source Files
- `controller.ubp`: Car receiver program. It listens for incoming BLE messages and adjusts servo positions to control car movement.
- `AI-assisted recognition system.ubp`: Transmitter program. It reads sensor inputs, computes control values, and sends commands to the car via BLE radio.

## How to Deploy
1. Install the MicroBlocks IDE
2. Open the two `.ubp` project files separately
3. Flash `AI-assisted recognition system.ubp` to the transmitter ESP32
4. Flash `controller.ubp` to the receiver ESP32
5. Ensure both boards use the same BLE radio group number
6. Power up both boards, then the recognition module can wirelessly control the smart car.

## Notes
- `.ubp` is MicroBlocks project file, cannot be opened with Arduino IDE.
- Both boards must be powered on to establish BLE connection.

