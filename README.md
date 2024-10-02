# TurtleBot-Perception-Integration

---

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
