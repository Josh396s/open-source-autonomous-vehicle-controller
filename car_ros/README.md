All work is done using Ubuntu 20.04
Must have ROS2 Foxy installed (Reference https://youtu.be/uWzOk0nkTcI)
Must have Gazebo installed (Reference https://classic.gazebosim.org/tutorials?tut=install_ubuntu)

Steps:
1) Input the command "source install/setup.bash" in order to make the robot discoverable (Must be done for every new terminal tab)
2) Input the command "colcon build --cmake-clean-cache --symlink-install" to build the robot 
3) Launch RVIZ2 with the command "rviz2"
4) In a new tab, change into the 'worlds' directory
5) Launch Gazebo with command "ros2 launch articubot_one launch_sim.launch.py world:=racetrack.world"
6) In the RVIZ2 window, hit File->Open Config->config->drive_bot.rviz  (Note: Program is buggy and won't spawn the vehicle at times, if that's the case close and rerun RVIZ2)
7) In a new tab, launch the keyboard control with command "ros2 run teleop_twist_keyboard teleop_twist_keyboard" (Must be on this tab when controlling the robot in order to make the robot move)

REFERENCES:
-Creating 3D model of a robot with URDF (https://youtu.be/BcjHyhV0kIs)
-Importing/Driving robot in Gazebo (https://youtu.be/IjFcr5r0nMs)
-Sensor/Driver Plugins (https://classic.gazebosim.org/tutorials?tut=ros_gzplugins)