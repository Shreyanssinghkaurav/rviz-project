# 🚀 Autonomous Exploration Rover Using SLAM and Optimal Path Planning in ROS

## 📌 Project Overview

This project implements a fully autonomous rover capable of exploring unknown environments using SLAM (Simultaneous Localization and Mapping) and optimal path planning in ROS 2.

The rover can:

* Build a map of unknown environments in real-time
* Localize itself within the map
* Navigate autonomously to goal points
* Avoid obstacles without human intervention
* Visualize everything using RViz

The system runs entirely in Gazebo simulation, requiring no physical robot.

---

## 🧠 System Architecture

The system consists of multiple layers:

* Simulation Layer (Gazebo)
* Sensor Layer (LIDAR, camera, encoders)
* Mapping Layer (SLAM Toolbox)
* Navigation Layer (Nav2)
* Control Layer (ros2_control)
* Visualization Layer (RViz)

---

## 🤖 Robot Design

### Core Components

* Base frame (base_link)
* Differential drive system
* Chassis with collision and inertia

### Sensors

* LIDAR (360° scanning) → `/scan`
* Wheel encoders → `/odom`
* Camera → `/camera/image_raw`

---

## ⚙️ Software Stack

* ROS 2 (Humble)
* Gazebo Harmonic
* SLAM Toolbox
* Nav2 Stack
* RViz
* ros2_control

---

## 🔄 Working Flow

1. Launch simulation in Gazebo
2. Spawn robot into environment
3. Sensors start publishing data
4. SLAM builds map in real-time
5. Navigation stack initializes
6. User sets goal in RViz
7. Planner computes optimal path
8. Controller executes motion
9. Robot reaches goal autonomously

---

## ⚠️ Challenges Solved

* Migration from Gazebo Classic to Gazebo Harmonic
* OpenGL issues in virtual machine
* Plugin compatibility updates
* Sensor data publishing issues
* TF frame mismatches
* Controller conflicts

---

## 📊 Key Concepts

* SLAM (Mapping + Localization)
* Path Planning (A*)
* ROS 2 Topics and TF
* Autonomous Navigation (Nav2)
* Robot Modeling (URDF/Xacro)
* Simulation Integration

---

## 🎯 Future Improvements

* Real-world robot deployment
* Computer vision integration
* Multi-robot coordination
* AI-based navigation

---

## 📌 Summary

This project demonstrates a complete autonomous robotics pipeline combining perception, mapping, planning, and control using modern ROS 2 tools.

---
