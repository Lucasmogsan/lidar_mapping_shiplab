# LiDAR mapping using RTABMAP

Using RTABMAP to generate a map and perform SLAM.

TODO:
- Deskewing not working
- Any other dependencies needed?


# Requirements
| Requirement | Version |
|-------------|---------|
| Operating System | Ubuntu 22.04 |
| ROS2        | Humble  |
| Python      | >=3.9.0 |

# Dependencies
The package depends on the following ROS2 capabilities:
```bash
sudo apt install ros-humble-rtabmap-ros
```


# Running the code:
Make sure to be running bag/node containing:
Topic: os_lidar
Frame: /ouster/points

Start RTABMAP from launch script:
```bash
ros2 launch lidar_map ouster.launch.py
```

Replay bag with clock:
```bash
ros2 bag play $BAGNAME --clock
```

Visualize single scans in RVIZ (optional):
Run rviz2 and open config file in this repos rviz folder.
