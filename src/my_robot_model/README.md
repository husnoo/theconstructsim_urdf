
## my_robot_model repository
Date: November 2022
License: BSD-3-Clause

## Description
This respository contains demo files required by the ROS2 URDF course.
Students must clone this respository into their `ros2_ws` workspace as instructed by the course.


Build and source the workspace:

```
cd ~/ros2_ws/; colcon build --packages-select my_robot_model; source install/setup.bash
```

Start a simulation:  

```
ros2 launch my_robot_model start_world.launch.py
```

Then in a new webshell spawn the robot:    

```
source ~/ros2_ws/install/setup.bash; ros2 launch my_robot_model spawn_robot_ros2.launch.xml

```





