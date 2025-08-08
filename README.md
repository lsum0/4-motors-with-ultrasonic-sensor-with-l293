# 🤖 Robotic System Simulation with Obstacle Avoidance

## 🔍 Overview

This project demonstrates a simulated robotic system powered by **4 DC motors**, an **L293D motor driver**, a **servo motor**, and an **ultrasonic sensor**. The robot performs directional movements and responds to obstacles in real-time using distance measurements.

---

## 🎯 Objectives

Using the **L293D motor driver**, the system is programmed to:

- 🔼 Move **forward** for **30 seconds**
- 🔽 Move **backward** for **1 minute**
- 🔁 Perform **alternating left and right turns** for **1 minute**
- 🚧 **Detect obstacles** within **10 cm** using the **HC-SR04** ultrasonic sensor
- 🔁 **Stop and change direction** automatically upon detection
- 🎯 Trigger the **servo motor** to react based on sensor input

---

## ⚙️ Components Used

- Arduino Uno  
- L293D Motor Driver Shield  
- 4 × DC Motors  
- 1 × Servo Motor  
- 1 × Ultrasonic Sensor (HC-SR04)  
- Breadboard  
- Jumper Wires  
- Power Supply (5V)  

---

## 🛠 Tools & Platforms

- **Tinkercad Circuits** – for simulating the circuit  
- **Arduino IDE** (within Tinkercad) – for writing and uploading code  

---

## 🚦 Features

- ✅ **Directional control** of 4 DC motors (forward, backward, turning)
- 📏 **Real-time obstacle detection** (≤10 cm) using ultrasonic sensor
- 🔄 **Automatic stop and redirection** when an object is near
- 🎮 **Servo motor action** triggered by object detection
- 🌐 **Fully virtual** – No physical hardware needed, runs entirely on Tinkercad

---

## ▶️ How to Use

1. **Open** the simulation in [Tinkercad Circuits](https://www.tinkercad.com/)
2. **Connect components** as follows:
   - DC motors → L293D output pins  
   - Ultrasonic sensor → Arduino digital pins  
   - Servo motor → Arduino PWM pin
3. **Upload the code** using Arduino IDE inside Tinkercad
4. Click **Start Simulation**
5. **Observe** the robotic behavior and automatic reactions to nearby objects

---

## 🧠 Use Cases

This robotic simulation can be used for:

- 🤖 Developing **object-avoiding robots**
- 🎓 Building **educational prototypes** in robotics
- 🧪 **Testing motor driver logic** (L293D)
- 🚀 Practicing embedded systems programming & automation logic

---

> 💡 *Great for students, hobbyists, and beginners in robotics and Arduino projects.*
