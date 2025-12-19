# Hand Gesture RC Car

Control an RC car with hand gestures using ESP32 and MPU6050 accelerometer! This project enables intuitive wireless control by simply tilting your hand in different directions.

##  Features

- **Wireless Control**: WiFi-based communication between controller and car
- **Intuitive Gestures**: Natural hand movements control car direction
- **Real-time Response**: Low-latency gesture detection and motor control
- **Dual ESP32 Setup**: One for the hand controller, one for the car
- **Accelerometer-based**: Uses MPU6050 for precise tilt detection

## Gesture Controls

For Forward = Tilt  Forward
FOR Backward = Tilt Reverse
FOR Left = Tilt Left
FOR Right = Tilt Right
To stop = Hand at Rest (x=0, y=0, z=0)
## 🔧 Hardware Requirements

### Controller Unit
- ESP32 Development Board x1
- MPU6050 Accelerometer Module x1
- 9V Battery x1
- Connecting Wires
- Breadboard (optional)

### Car Unit
- ESP32 Development Board x1
- L298N Motor Driver Module x1
- DC Motors x2 (or x4 for 4WD)
- 3.7V Lithium-Ion Battery x3 (11.1V battery pack)
- Robot Car Chassis
- Wheels
- Connecting Wires

## Circuit Diagram
in read me for circuit diagram 
### Controller Connections
In read me for connections 

## Software Requirements

- Arduino IDE (1.8.x or later)
- ESP32 Board Package
- Required Libraries:
  - `Wire.h` (built-in)
  - `MPU6050.h` (by Electronic Cats or Adafruit)
  - `WiFi.h` (built-in with ESP32)

##  Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/hand-gesture-rc-car.git
   cd hand-gesture-rc-car
   ```

2. **Install Arduino IDE**
   - Download from [arduino.cc](https://www.arduino.cc/en/software)

3. **Setup ESP32 in Arduino IDE**
   - Go to `File` → `Preferences`
   - Add to Additional Board Manager URLs:
   - Go to `Tools` → `Board` → `Boards Manager`
   - Search for "ESP32" and install

4. **Install Required Libraries**
   - Go to `Sketch` → `Include Library` → `Manage Libraries`
   - Search and install:
     - MPU6050 library

5. **Configure WiFi Credentials**
   - Open both `controller.ino` and `car.ino`
   - Update WiFi SSID and password:
     ```cpp
     const char* ssid = "YOUR_SSID";
     const char* password = "YOUR_PASSWORD";
     ```

6. **Upload Code**
   - Connect Controller ESP32 → Upload `controller.ino`
   - Connect Car ESP32 → Upload `car.ino`

##  Usage

1. **Power On**
   - Turn on the car (ensure battery is charged)
   - Turn on the controller

2. **Wait for Connection**
   - Both ESP32s will connect to WiFi
   - LED indicators (if implemented) will show connection status

3. **Control the Car**
   - Hold the controller in your hand naturally
   - Tilt your hand in the direction you want the car to move
   - Keep your hand level to stop the car

4. **Tips**
   - Start with gentle tilts to get familiar with sensitivity
   - Ensure clear WiFi signal between controller and car
   - Calibrate MPU6050 if needed for better accuracy

## Troubleshooting

**Car not responding:**
- Check WiFi connection on both ESP32s
- Verify battery voltage (should be above 10V)
- Check motor driver connections

**Erratic movements:**
- Calibrate MPU6050 sensor
- Check for loose connections
- Reduce WiFi interference

**Motors not running:**
- Check L298N power supply
- Verify motor connections
- Test motors directly with battery

## 📂 Project Structure


hand-gesture-rc-car/
├── controller/
│   └── controller.ino          # Hand controller code
├── car/
│   └── car.ino                 # RC car code
├── circuit_diagram/
│   ├── controller_circuit.png  # Controller wiring
│   └── car_circuit.png         # Car wiring
├── images/
│   └── demo.gif                # Demo video/gif
└── README.md


##  License

This project is open source and available under the [MIT License](LICENSE).

##  Credits

**Created by:** Varun Goel



---

⭐ If you found this project helpful, please consider giving it a star!

**Happy Building! 🚗✨**
