# ROS Extended Kalman Filter POC

This project uses the ROS navigation stack to test out the EKF capabilities.

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
