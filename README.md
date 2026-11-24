<!--
  ✏️ HOW TO USE
  1. Put this README.md and the `assets/` folder in the root of your repo (or your profile repo).
  2. Social / website links are intentionally EMPTY: fill the `()` after each badge, e.g. [![Website](...)](https://your-site.com)
  3. Progress bars: open assets/progress.svg and change the `to="..."` values + the "%" text.
  4. Typing text: open assets/typing.svg (4 lines) or just replace the text in it.
  5. Delete any badge or section you don't need.
-->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0A0A0A,100:E01B24&height=140&section=header&animation=fadeIn" width="100%" alt="">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/amotron_logo_dark.svg">
  <img src="assets/amotron_logo.svg" alt="AMOTRON logo" width="480">
</picture>

<br/>

<img src="assets/typing.svg" alt="AMOTRON tagline" width="620">

<br/>

**Advanced · Mechanical · Operations · Technology & Robotics Oriented Network**

<br/>

![Team](https://img.shields.io/badge/AMOTRON-Robotics%20Team-E01B24?style=for-the-badge&logo=robotframework&logoColor=white)
![Project](https://img.shields.io/badge/Project-Line%20Following%20Robot-0A0A0A?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange?style=for-the-badge)
![Language](https://img.shields.io/badge/Code-C%2FC%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

<br/>

<!-- 🔗 Fill in your links inside the () -->
[![Website](https://img.shields.io/badge/Website-0A0A0A?style=for-the-badge&logo=googlechrome&logoColor=white)]()
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)]()
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)]()
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)]()
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)]()
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)]()
[![TikTok](https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white)]()
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)]()
[![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)]()
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)]()

</div>

<img src="assets/divider.svg" width="100%" alt="">

## 📖 Table of Contents

[About](#-about-amotron) · [Project](#-current-project-line-following-robot-lfr) · [Progress](#-live-progress) · [Team](#-team) · [Tech Stack](#️-tech-stack) · [Roadmap](#-roadmap) · [Gallery](#-gallery) · [Contact](#-get-in-touch)

<img src="assets/divider.svg" width="100%" alt="">

## 🤖 About AMOTRON

<table>
<tr>
<td width="260" align="center">
  <img src="assets/amotron_logo_animated.gif" alt="AMOTRON animated logo" width="240">
</td>
<td>

**AMOTRON** is a student robotics team passionate about turning ideas into working machines. We design, build, test, and improve robots, and we are preparing to compete in robotics competitions.

| Letter | Meaning |
|:---:|:---|
| **A** | Advanced |
| **M** | Mechanical |
| **O** | Operations |
| **TRON** | Technology & Robotics Oriented Network |

</td>
</tr>
</table>

<img src="assets/divider.svg" width="100%" alt="">

## 🏁 Current Project: Line Following Robot (LFR)

<div align="center">

<img src="assets/lfr_track.svg" alt="Animated line following robot" width="100%">

</div>

We are building an **autonomous Line Following Robot** that can detect a track and follow it quickly, smoothly, and accurately.

### 🎯 Objectives

- 🔴 Develop a fully autonomous Line Following Robot
- ⚙️ Implement sensor-based line detection
- 💻 Improve control logic in C/C++
- 🔌 Work with embedded systems and electronic components
- 🏎️ Optimize speed, stability, and accuracy
- 🧪 Test, troubleshoot, and improve real-world performance

### 🧩 How It Works

```mermaid
flowchart LR
    A[IR Sensor Array] --> B[Microcontroller]
    B --> C[Control Logic - PID]
    C --> D[Motor Driver]
    D --> E[Motors & Wheels]
    E -.->|feedback| A
```

### 🔧 Hardware & Components

<!-- Fill this in as you finalize your build -->

| Part | Details |
|:---|:---|
| Microcontroller | _to be added_ |
| Sensors | _to be added_ |
| Motor Driver | _to be added_ |
| Motors | _to be added_ |
| Power | _to be added_ |

<details>
<summary><b>💻 Sample control logic (PID skeleton, click to expand)</b></summary>

<br/>

A simplified Arduino-style skeleton to show the idea. Replace pins, sensor weights, and PID constants with your own after calibration.

```cpp
// Example only: tune every value on your own robot
float Kp = 0.0, Ki = 0.0, Kd = 0.0;   // set after calibration
int   baseSpeed = 150;
float lastError = 0, integral = 0;

int readLinePosition() {
  // return a value like -3 (far left) ... 0 (center) ... +3 (far right)
  // based on your sensor array
  return 0;
}

void loop() {
  int   error = readLinePosition();
  integral   += error;
  float pid   = Kp * error + Ki * integral + Kd * (error - lastError);
  lastError   = error;

  int leftSpeed  = constrain(baseSpeed + pid, 0, 255);
  int rightSpeed = constrain(baseSpeed - pid, 0, 255);
  setMotors(leftSpeed, rightSpeed);   // your motor driver function
}
```

</details>

<img src="assets/divider.svg" width="100%" alt="">

## 📊 Live Progress

<div align="center">

<img src="assets/progress.svg" alt="LFR project progress" width="720">

</div>

<img src="assets/divider.svg" width="100%" alt="">

## 👥 Team

<div align="center">

| Member | Role | GitHub |
|:---:|:---|:---:|
| **Abdulla-al-Noman Orko** | Robotics, Electronics & Programming | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github)]() |
| **Mahir Sufian** | Robot Development & Team Collaboration | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github)]() |
| **Ahammad Ibna Mazhar** | Robot Development & Team Collaboration | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github)]() |

</div>

<img src="assets/divider.svg" width="100%" alt="">

## 🛠️ Tech Stack

<div align="center">

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Robotics](https://img.shields.io/badge/Robotics-181717?style=for-the-badge&logo=robotframework&logoColor=red)
![Electronics](https://img.shields.io/badge/Electronics-E01B24?style=for-the-badge)
![Embedded Systems](https://img.shields.io/badge/Embedded%20Systems-333333?style=for-the-badge)

</div>

<img src="assets/divider.svg" width="100%" alt="">

## 📌 Roadmap

- [x] Team formation
- [x] Project planning
- [x] Initial research & design
- [ ] Robot assembly
- [ ] Sensor integration
- [ ] Programming & calibration
- [ ] Track testing
- [ ] Performance optimization
- [ ] Competition participation

<img src="assets/divider.svg" width="100%" alt="">

## 📸 Gallery

<!-- Add your robot photos here, for example:
<p align="center">
  <img src="assets/robot-1.jpg" width="30%">
  <img src="assets/robot-2.jpg" width="30%">
  <img src="assets/robot-3.jpg" width="30%">
</p>
-->

_Photos and demo videos coming soon._

<img src="assets/divider.svg" width="100%" alt="">

## ❓ FAQ

<details>
<summary><b>What is AMOTRON?</b></summary>
<br/>
A student robotics team: <b>A</b>dvanced <b>M</b>echanical <b>O</b>perations + <b>T</b>echnology &amp; <b>R</b>obotics <b>O</b>riented <b>N</b>etwork.
</details>

<details>
<summary><b>What are you building right now?</b></summary>
<br/>
An autonomous Line Following Robot (LFR) for robotics competitions.
</details>

<details>
<summary><b>Can I collaborate or sponsor the team?</b></summary>
<br/>
Yes, please reach out through any of the links above.
</details>

<img src="assets/divider.svg" width="100%" alt="">

## 🤝 Get in Touch

Want to collaborate, sponsor, or just say hi? Reach out through any of the links at the top of this page.

<div align="center">

<br/>

<img src="assets/amotron_icon.png" alt="AMOTRON icon" width="90">

### **Building our ideas into reality, one circuit, one sensor, and one line of code at a time.**

<br/>

[![Website](https://img.shields.io/badge/Website-0A0A0A?style=flat-square&logo=googlechrome&logoColor=white)]()
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=flat-square&logo=facebook&logoColor=white)]()
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white)]()
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)]()
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)]()

<br/>

⭐ If you like our work, give this repo a star ⭐

<br/>

© 2026 **AMOTRON** · All rights reserved

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0A0A0A,100:E01B24&height=120&section=footer" width="100%" alt="">

</div>
