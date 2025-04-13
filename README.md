# TurtleBot-Perception-Integration

This repository contains ROS2 (Humble) package developed for the Turtlebot Waffle perception and planning challenge as part of the **ENPM673: Perception for Autonomous Robots** course (Spring 2024) at the University of Maryland.

---

## Project Overview

The project focuses on the integration of advanced perception algorithms and planning techniques to enable autonomous navigation for a Turtlebot equipped with a color camera. The key challenges addressed include:

### Projective Geometry
- Detects horizon line using parallel line intersection and vanishing point calculation.
- Visualizes detected horizon line in real-time.

### Object Detection (Stop Sign)
- Implements stop sign detection with YOLOv5.
- Draws bounding boxes and indicates detection status.
- Stops the robot when a stop sign is confidently detected.

### Dynamic Obstacle Detection
- Utilizes optical flow to identify dynamic obstacles.
- Marks obstacles as "above" or "below" the horizon line.
- Stops robot movement upon detecting obstacles below the horizon line.

### Autonomous Navigation
- Calculates waypoints dynamically using visual cues.
- Adjusts robot movement based on the position of detected lanes and obstacles.
- Performs real-time trajectory correction using planning algorithms.

## Gazebo Implementation

https://github.com/Abhey16/TurtleBot-Perception-Integration/assets/132549463/2a4b8be9-32b5-4a3f-826b-779dacaab7e1

## Turtlebot3 Implementation

https://github.com/user-attachments/assets/377f27e5-7e44-462b-aeee-3ec29c4653d1

## Installation
Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.
1. Create a directory with a subfolder named **src** on your local machine.
2. Navigate into the directory using Terminal and run:
```
colcon build
```
This will convert your directory into a ROS2 Workspace

3. Navigate to the src folder and clone the repository to your local machine:
```
https://github.com/Abhey16/TurtleBot-Perception-Integration.git
```
This will add ROS package in the **src** folder. Remember to add only the package not the CAD files(which are provided only for reference)

4. Navigate to the root of ROS2 directory and build the project using colcon:
```
colcon build
```
5. Source the environment to set up the necessary ROS2 variables:
```
source install/setup.bash
```
6. Now launch the Gazebo environment
```
ros2 launch enpm673_final_proj enpm673_world.launch.py 
```
7. For navigation script run:
```
ros2 run perception percept  
```
