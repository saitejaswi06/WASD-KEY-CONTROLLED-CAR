# 🚗 WASD-Controlled RC Car | ESP8266 + L293D + Arduino IDE

A Wi-Fi-enabled robotic car controlled using **WASD keyboard inputs**, where commands are sent wirelessly to an ESP8266 NodeMCU, driving a differential motor setup via the L293D motor driver.

## ⚙️ Technologies & Components Used
| Component        | Purpose                                 |
|------------------|-----------------------------------------|
| ESP8266 NodeMCU  | Wi-Fi microcontroller (control unit)   |
| L293D Motor Driver| Drives the left and right DC motors    |
| DC Gear Motors   | Differential drive motion              |
| HTML Web Server  | Receives WASD inputs via Wi-Fi         |
| Arduino IDE      | Programmed the ESP8266 firmware        |
| Power Supply     | 7.4V LiPo / battery pack for motors    |

## 🛠️ System Overview
- ESP8266 hosts an **HTML web server** with a simple UI or listens for **WASD commands** from a client (PC/Phone).
- Upon receiving a keypress (`W`, `A`, `S`, `D`), the ESP8266:
   - Sets the motor direction and speed through the L293D motor driver.
   - Supports forward (`W`), reverse (`S`), left (`A`), and right (`D`) movement.
- Communication uses Wi-Fi, making the robot wirelessly controllable within the network range.

## 🔌 Control Flow
1. ESP8266 starts as an **Access Point (AP)** or connects to Wi-Fi.
2. Hosts a webpage or processes HTTP GET requests for control.
3. Motor pins are toggled based on received key input:
   - **W** → Both motors forward.
   - **A** → Left motor reverse, right motor forward (left turn).
   - **D** → Left motor forward, right motor reverse (right turn).
   - **S** → Both motors reverse.

## ✅ Key Features
- Simple wireless control using a keyboard or mobile browser.
- Fully customizable control interface (HTML/CSS/JS).
- Differential drive supports smooth turns.
- Compact and affordable ESP8266-based build.

## 🔧 Future Improvements
- Add speed control via PWM.
- Upgrade to WebSocket for real-time input handling.
- Implement collision detection with ultrasonic sensors.

