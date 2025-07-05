---
layout: post
title: "Smart Light Control with ESP32"
description: "A DIY IoT project using ESP32 to control lights based on motion."
date: 2025-06-28
tags: [ESP32, IoT, Arduino, Smart Home]
image: /images/smartlight-banner.jpg
description: "Smart light project using IoT."
category: Projects
---

<img src="/images/smartlight-banner.jpg" alt="Smart Light Banner" style="width:100%; border-radius: 12px; margin-bottom: 20px;">

## 🔍 Project Overview

In this project, we’ll create a smart light system using an ESP32 board and a PIR motion sensor.  
When motion is detected, the light turns on automatically!

---

## ▶️ Demo Video

<div align="center">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/YOUR_VIDEO_ID" frameborder="0" allowfullscreen></iframe>
</div>

---

## 🧠 How It Works

- The **PIR sensor** detects motion
- ESP32 sends a signal to switch the LED
- Can be expanded to real AC bulbs with a relay module

---

## 🧰 Materials Used

- ESP32 Dev Board  
- PIR Motion Sensor  
- Breadboard + Jumper Wires  
- LED + Resistor  
- USB Cable

---

## 💻 Arduino Code

```cpp
#define PIR 12
#define LED 13

void setup() {
  pinMode(PIR, INPUT);
  pinMode(LED, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  if (digitalRead(PIR) == HIGH) {
    digitalWrite(LED, HIGH);
    Serial.println("Motion Detected");
    delay(5000); // keep light on for 5 seconds
    digitalWrite(LED, LOW);
  }
}
