# ROS Extended Kalman Filter POC

This project uses the ROS navigation stack to test out the EKF capabilities.

A turtlebot is simulated in a gazebo world. The unfiltered trajectory (from the motor encoder) and the filtered EKF trajectory are plotted side by side in RViz for comparison. To command the robot, the turtle teleop package is used.

<img width="1624" alt="gazebo-screenshot" src="https://user-images.githubusercontent.com/3985351/161390596-37a0c77c-c13d-4ae5-a793-a3da31b4e199.png">

![rviz-screenshot](https://user-images.githubusercontent.com/3985351/161390601-1e5323b3-6402-4528-b892-2dc38b5f4413.jpg)


**ROS Version**: Kinetic

**Commands to run**:

*Run each launch in a separate terminal*

    cd /mnt/Workspaces/kalman-filter-poc/catkin_ws
    source devel/setup.bash
    roslaunch turtlebot_gazebo turtlebot_world.launch
    roslaunch robot_pose_ekf robot_pose_ekf.launch
    roslaunch odom_to_trajectory create_trajectory.launch
    roslaunch turtlebot_teleop keyboard_teleop.launch
    roslaunch src/RvizLaunch.launch

*Alternatively, use the main launcher*

    cd /mnt/Workspaces/kalman-filter-poc/catkin_ws
    source devel/setup.bash
    roslaunch main main.launch
    
    
The pre-configured RViz file is located in `/mnt/Workspaces/kalman-filter-poc/catkin_ws/src/EKFLab.rviz` and this should be updated in the RViz launch file and/or the main launch file.
