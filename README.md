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



```Text


int trigger_pin = 6;
int echo_pin = 3;
int in1=2;
int in2=5;
;
int in3=10;
int in4=12;

int in5=4;
int in6=7;

int in7=8;
int in8=13;
int distance;

int time;


void setup()
{
  Serial.begin(9600);
  pinMode(trigger_pin, OUTPUT);
  pinMode(echo_pin, INPUT);
  
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
  pinMode(in3, OUTPUT);
  pinMode(in4, OUTPUT);
  
  pinMode(in5, OUTPUT);
  pinMode(in6, OUTPUT);
  pinMode(in7, OUTPUT);
  pinMode(in8, OUTPUT);
  
}
void loop(){
  
    digitalWrite (trigger_pin, HIGH);

    delayMicroseconds (10);

    digitalWrite (trigger_pin, LOW);

    time = pulseIn (echo_pin, HIGH);

    distance = (time * 0.034) / 2;
    if(distance >= 50){
          Serial.println("objection not  detected");
          Serial.print("Distance=");
          Serial.println(distance);
          digitalWrite(in1,HIGH);
          digitalWrite(in2,LOW);
          digitalWrite(in3,HIGH);
          digitalWrite(in4,LOW);
          
          
          digitalWrite(in5,HIGH);
          digitalWrite(in6,LOW);
          digitalWrite(in7,HIGH);
          digitalWrite(in8,LOW);
          
          delay(500);
    }
  
  else{
          Serial.println("objection  detected");
          Serial.print("Distance=");
          Serial.println(distance);
          digitalWrite(in1,LOW);
          digitalWrite(in2,LOW);
          digitalWrite(in3,HIGH);
          digitalWrite(in4,LOW);
          
          
          digitalWrite(in5,LOW);
          digitalWrite(in6,LOW);
          digitalWrite(in7,HIGH);
          digitalWrite(in8,LOW);
          
     
          
          delay(500);
  }
}
```


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
