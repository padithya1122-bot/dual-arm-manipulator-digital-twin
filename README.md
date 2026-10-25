# Design and Simulation of a Dual-Arm Robotic Manipulator with Coordinate Motion Control in NVIDIA Omniverse

This repository contains the complete workflow, documentation, and presentation materials for the **Mini Project** titled *"Design and Simulation of a Dual-Arm Robotic Manipulator with Coordinate Motion Control in NVIDIA Omniverse"*, conducted at **SASTRA Deemed to be University** (School of Mechanical Engineering).

* **Author:** Perugu Venkata Aditya
* **Program:** B.Tech – Mechanical Engineering (Digital Manufacturing)
* **Project Guide:** Dr. Hari Krishnan R, Assistant Professor – III

---

## 📌 Project Overview
Testing control code directly on physical hardware can be slow, costly, and risky (leading to potential collisions, gravity collapse, or equipment wear). This project solves this challenge by developing a physics-accurate **digital twin** of a 12-DOF dual-arm robotic manipulator mounted on a mobile base. 

The digital twin runs inside **NVIDIA Omniverse (Isaac Sim)** using GPU-accelerated PhysX rigid-body dynamics and communicates in real time via **ROS2** middleware using the exact same commands as the physical asset.

---

##  Tech Stack & Tools
* **CAD Modelling:** SolidWorks
* **URDF Exporter:** SW2URDF (translating links, joints, mass, inertia, limits, and dynamics)
* **Simulation Engine:** NVIDIA Omniverse Isaac Sim (PhysX)
* **Middleware & Communication:** ROS2 (DDS publish/subscribe nodes, Action Graphs / OmniGraph)
* **Kinematics Framework:** Denavit–Hartenberg (DH) Convention

---

##  Methodology (10-Step Pipeline)
1. **CAD Model Design:** SolidWorks assembly with accurate dimensions and designated link hierarchies.
2. **Kinematic Definition:** Assigning frames and coordinate systems using the Denavit–Hartenberg (DH) convention for 6-DOF per arm.
3. **URDF Generation:** Exporting physical properties (mass tensors, inertia matrices, damping, friction, and joint limits).
4. **Isaac Sim Import:** Loading the robot model and configuring the Articulation Root.
5. **Model Validation:** Verifying joint motion and limits using the PhysX Physics Inspector.
6. **ROS2 Integration:** Establishing real-time communication bridges.
7. **Base & Arm Control:** Setting up OmniGraph Action Graphs for joint-level control and differential drive base control.
8. **Environment & Sensor Integration:** Building the virtual cell workspace.
9. **Hardware vs. Simulation Comparison:** Executing trial trajectories on both the physical asset and the digital twin.
10. **Accuracy Analysis:** Quantifying positional deviations and percentage accuracy.

---

##  Key Results & Performance Accuracy
The twin was validated across 5 trials per arm against the physical robot by recording end-effector coordinates ($X, Y, Z$) under identical command vectors:

* **Right Arm Average Positional Accuracy:** **96.60%**
* **Left Arm Average Positional Accuracy:** **96.20%**
* **Mean Absolute Axis Deviations:**
  * *Right Arm:* $X = 12.4\text{ mm}$, $Y = 7.6\text{ mm}$, $Z = 9.8\text{ mm}$
  * *Left Arm:* $X = 13.4\text{ mm}$, $Y = 7.2\text{ mm}$, $Z = 12.7\text{ mm}$

---

## 📂 Repository Contents & Links
* `Miniproject_Dual_Arm_Digital_Twin_Perugu_Venkata_Aditya.pptx`: Comprehensive final viva slide deck.
  * [Presentation Slide Link](https://docs.google.com/presentation/d/1v2APEwEOzkVg5de8Gst7XL1t7O7VuYG1/edit?usp=drive_link&ouid=110186731700141658012&rtpof=true&sd=true)
* `Miniproject_Report_Dual_Arm_Digital_Twin_Perugu_Venkata_Aditya.docx`: Complete mini project report detailing mathematical derivations, trial data tables, and error calculations.
  * [Project Report Document Link](https://docs.google.com/document/d/1vGa9ArsqJ09pYVqdJuxIU99vat_HgFuT/edit?usp=drive_link&ouid=110186731700141658012&rtpof=true&sd=true)
