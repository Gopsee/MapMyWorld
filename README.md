# MapMyWorld

This is a Mapping and SLAM project, We create a 2D occupancy grid and 3D octomap from a simulated environment using mobile robot with the RTAB-Map (Real-Time Appearance-Based Mapping). RTAB-Map is a popular solution for SLAM to develop robots that can map environments in 3D. RTAB-Map has good speed and memory management, and it provides custom developed tools for information analysis.

### Description
We have two ROS packages in this project, one is custom build packge (my_robot) and the other is rtab_map, which will be used for mapping and SLAM purpose. We have our my_robot node interacting with rtab_map node to perform the SLAM, Mapping and Localization as per the requirement.

## Basic Build Instruction

1. Create a catkin Workspace
```
    mkdir -p catkin_ws/src
    cd catkin_ws/src
    catkin_init_workspace
    cd ..
    catkin_make
```

2. Clone the repository
```
    cd catkin/src
    git clone https://github.com/Gopsee/MapMyWorld.git
    cd ..
    catkin_make
 ```
 
 3. source the workspace
 ```
    source devel/setup.bash
 ```
 
 4. Launch the node
 ```
      roslaunch my_robot world.launch
      roslaunch my_robot teleop.launch
      roslaunch my_robot mapping.launch
  ```
 
 ### RTAB_MAP for Localization
 
This same package could be used for performing Localization alone. This requires change of values for a few parameter in the       mapping.launch file.
```
    roslaunch my_robot world.launch
    roslaunch my_robot localization.launch
```


 

