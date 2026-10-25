# Design and Simulation of a Dual-Arm Robotic Manipulator with Coordinate Motion Control in NVIDIA Omniverse

This repository contains the complete workflow, documentation, and presentation materials for the **Mini Project** titled *"Design and Simulation of a Dual-Arm Robotic Manipulator with Coordinate Motion Control in NVIDIA Omniverse"*[cite: 5, 6], conducted at **SASTRA Deemed to be University** (School of Mechanical Engineering)[cite: 5, 6].

* **Author:** Perugu Venkata Aditya[cite: 5, 6]
* **Program:** B.Tech – Mechanical Engineering (Digital Manufacturing)[cite: 5, 6]
* **Project Guide:** Dr. Hari Krishnan R, Assistant Professor – III[cite: 5, 6]

---

## 📌 Project Overview
Testing control code directly on physical hardware can be slow, costly, and risky (leading to potential collisions, gravity collapse, or equipment wear)[cite: 5]. This project solves this challenge by developing a physics-accurate **digital twin** of a 12-DOF dual-arm robotic manipulator mounted on a mobile base[cite: 5, 6]. 

The digital twin runs inside **NVIDIA Omniverse (Isaac Sim)** using GPU-accelerated PhysX rigid-body dynamics and communicates in real time via **ROS2** middleware using the exact same commands as the physical asset[cite: 5, 6].

---

## 🛠️ Tech Stack & Tools
* **CAD Modelling:** SolidWorks[cite: 5]
* **URDF Exporter:** SW2URDF (translating links, joints, mass, inertia, limits, and dynamics)[cite: 5]
* **Simulation Engine:** NVIDIA Omniverse Isaac Sim (PhysX)[cite: 5]
* **Middleware & Communication:** ROS2 (DDS publish/subscribe nodes, Action Graphs / OmniGraph)[cite: 5]
* **Kinematics Framework:** Denavit–Hartenberg (DH) Convention[cite: 5]

---

## 🔄 Methodology (10-Step Pipeline)
1. **CAD Model Design:** SolidWorks assembly with accurate dimensions and designated link hierarchies[cite: 5].
2. **Kinematic Definition:** Assigning frames and coordinate systems using the Denavit–Hartenberg (DH) convention for 6-DOF per arm[cite: 5].
3. **URDF Generation:** Exporting physical properties (mass tensors, inertia matrices, damping, friction, and joint limits)[cite: 5].
4. **Isaac Sim Import:** Loading the robot model and configuring the Articulation Root[cite: 5].
5. **Model Validation:** Verifying joint motion and limits using the PhysX Physics Inspector[cite: 5].
6. **ROS2 Integration:** Establishing real-time communication bridges[cite: 5].
7. **Base & Arm Control:** Setting up OmniGraph Action Graphs for joint-level control and differential drive base control[cite: 5].
8. **Environment & Sensor Integration:** Building the virtual cell workspace[cite: 5].
9. **Hardware vs. Simulation Comparison:** Executing trial trajectories on both the physical asset and the digital twin[cite: 5].
10. **Accuracy Analysis:** Quantifying positional deviations and percentage accuracy[cite: 5].

---

## 📊 Key Results & Performance Accuracy
The twin was validated across 5 trials per arm against the physical robot by recording end-effector coordinates ($X, Y, Z$) under identical command vectors[cite: 5, 6]:

* **Right Arm Average Positional Accuracy:** **96.60%**[cite: 5, 6]
* **Left Arm Average Positional Accuracy:** **96.20%**[cite: 5, 6]
* **Mean Absolute Axis Deviations:**
  * *Right Arm:* $X = 12.4\text{ mm}$, $Y = 7.6\text{ mm}$, $Z = 9.8\text{ mm}$[cite: 5, 6]
  * *Left Arm:* $X = 13.4\text{ mm}$, $Y = 7.2\text{ mm}$, $Z = 12.7\text{ mm}$[cite: 5, 6]

---

## 📂 Repository Contents
* `Miniproject_Dual_Arm_Digital_Twin_Perugu_Venkata_Aditya.pptx`: Comprehensive final viva slide deck[cite: 5].
* `Miniproject_Report_Dual_Arm_Digital_Twin_Perugu_Venkata_Aditya.docx`: Complete mini project report detailing mathematical derivations, trial data tables, and error calculations[cite: 6].
