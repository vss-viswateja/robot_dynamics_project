# Dynamic Gait Generation for a Quadruped Robot

This repository contains the files and resources for our capstone project in Robot Dynamics and Control.

## Project Description

This project focuses on creating a system that enables a quadruped robot to dynamically adjust its gait in real-time to navigate various terrains and adapt to changing conditions. Unlike traditional methods that rely on predefined gait cycles, this project aims to implement a system that allows the robot to walk, trot, or gallop efficiently while maintaining stability and adapting to external disturbances.

## Problem Statement

* **Inefficiency of Predefined Gaits:** Traditional quadruped robots often use fixed gait patterns that are not adaptable to real-world scenarios.
* **Instability on Complex Terrain:** Fixed gaits can lead to instability and falls when navigating rough or uneven terrain.
* **Challenge of Dynamic Balance Control:** Maintaining dynamic balance while moving requires precise control of the robot's center of mass (CoM).
* **Energy Consumption Optimization:** Poor gait design leads to excessive energy use, reducing the robot's operational efficiency.

## Solution and Procedure

The solution involves a multi-step approach to dynamically generate and adapt gaits:

1.  **Gait Selection:**
    * The system selects the appropriate gait based on speed and stability requirements:
        * Walking gait (4-beat cycle): High stability.
        * Trotting gait (2-beat cycle): Balanced speed and stability.
        * Galloping/bounding (1-beat cycle): High-speed motion.
2.  **Motion Trajectory Generation:**
    * Foot trajectories are computed based on desired velocity, obstacle positions, and ground reaction forces.
    * This is achieved using:
        * Inverse Kinematics (IK): To calculate joint angles for desired foot positions.
        * Trajectory Optimization: To ensure smooth movement transitions.
3.  **Stability and Balance Maintenance:**
    * To prevent falls, the system employs:
        * Zero Moment Point (ZMP) control: To keep forces within the support polygon.
        * Capture Point Control: To predict and adjust future steps dynamically.
        * Center of Mass (CoM) adjustment: To shift the robot's weight based on foot placement.
4.  **Real-time Adaptation via Control Methods:**
    * Dynamic adjustments are made using:
        * Model Predictive Control (MPC): To predict and adjust future movements.
        * Reinforcement Learning (RL): To learn and improve gait performance through AI.
        * Central Pattern Generators (CPG): To generate natural gait patterns.

## Dynamic Gait Changes

Dynamically changing the gait means the quadruped adapts its walking pattern in real-time based on:

* **Speed changes:** Transitioning between walking, trotting, and galloping.
* **Terrain variations:** Adjusting speed and gait based on terrain roughness.
* **External disturbances:** Modifying step timing and leg forces for recovery.
* **Energy efficiency:** Selecting the most efficient gait for a given task.

**Example:**

* On smooth ground, the robot uses a trotting gait for efficiency.
* On stairs or rocky terrain, it switches to a walking gait for stability.
* When encountering an obstacle, it dynamically adjusts step height or switches to a hopping gait.

## Expected Outcomes

* A quadruped robot that dynamically adjusts its gait to walk, trot, or gallop while maintaining stability and efficiency.
* The ability to navigate unpredictable terrain without predefined motion sequences.
* Energy-efficient locomotion for extended operation.




## Repository Structure

* **Resources/**: This folder holds essential learning materials, research papers, tutorials, and other resources relevant to the project.

## Resources

The `Resources/` folder currently includes:

* Null.

**Contribution:**

If you come across any useful resources related to Robot Dynamics and Control, please feel free to contribute by adding them to the `Resources/` folder. This will help improve the project's knowledge base and benefit other members.


## Author

* VSS Viswa Teja Bottu

