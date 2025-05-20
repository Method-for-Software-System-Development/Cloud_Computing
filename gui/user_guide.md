
# 🛠️ User Guide

Welcome to the **OptiLine Dashboard** — a real-time cloud-based interface for engineers in the CIM & Robotics Lab.

## 🔗 Quick Navigation
- [1. How to Use the System](#1-how-to-use-the-system)
- [2. Available Sensors](#2-available-sensors)
- [3. How to Earn Points](#3-how-to-earn-points)
- [4. FAQ](#4-faq)

---

## 1. How to Use the System

The dashboard consists of several main sections:

- **Live Sensors Dashboard**  
  Monitor real-time data from indoor and outdoor sensors.

- **Statistics Panel**  
  Analyze historical data using interactive plots. Select a date and time window to compare trends and spot irregular patterns.

- **MQTT Search Engine**  
  Search technical content directly from the [MQTT.com](https://mqtt.com) website. Use keywords to explore relevant documentation and topics.

- **Fault Simulator**  
  Practice diagnosing simulated production malfunctions and improve your troubleshooting skills.

- **User Directory**  
  View the contact information of authorized users in the system.

- **Leaderboard**  
  Track your cumulative performance points compared to other engineers in the lab.

---

## 2. Available Sensors

The following sensors are integrated into the system:

| Sensor Type               | Description                                                                 | Unit         | Location        |
|---------------------------|-----------------------------------------------------------------------------|--------------|-----------------|
| **Temperature**           | Measures ambient temperature                                                | °C           | Indoor & Outdoor|
| **Humidity**              | Measures relative air humidity                                              | %            | Indoor & Outdoor|
| **Pressure**              | Measures atmospheric pressure                                               | hPa          | Indoor          |
| **Daylight (Illuminance)**| Measures light intensity                                                    | Lux          | Outdoor         |
| **Distance (Ultrasonic)** | Ultrasonic sensor detects movement by measuring distance changes (e.g. people walking nearby) | mm          | Indoor          |

> *All sensors stream data in real time via MQTT protocol.*

---

## 3. How to Earn Points

Points are earned by successfully completing challenges in the **Fault Simulator**.

- 🧠 **Complexity-Based Scoring**  
  The more difficult and realistic the fault scenario, the higher the score upon successful resolution.

- ⏱️ **Time Efficiency**  
  Your time to complete all steps is tracked. Faster resolutions earn better standing on the leaderboard.

- ✅ **Full Completion Required**  
  You must complete **all steps** in the simulator to submit your solution. No partial credit is given.

- 🏆 **Cumulative Scoring**  
  Your total score accumulates over time and determines your position on the leaderboard.

---

## 4. FAQ

**Q: Can I skip steps in the Fault Simulator and still get points?**  
A: No. You must complete all required steps before submitting. Partial credit is not available.

**Q: Can I view or repeat previous faults?**  
A: Not at this stage. Handled faults cannot be revisited.

**Q: Are the sensors live or simulated?**  
A: Both modes are supported. In simulation mode, realistic data is streamed from a preloaded scenario.

**Q: How often is the leaderboard updated?**  
A: The leaderboard updates after each completed challenge, but the results are visible only after restarting the system.

---

Optimize wisely and climb the leaderboard! 🚀