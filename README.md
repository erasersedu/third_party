# third_party

Look at each author website for more references:

Crane Plus

https://gbiggs.github.io/ros_moveit_rsj_tutorial/manipulators_and_moveit.html


Dynamixel Motor

https://github.com/arebgun/dynamixel_motor

*

To Install:


> cd 

> mkdir -p ~/erasersedu_ws/src/

> cd ~/erasersedu_ws/src/

> git clone https://github.com/erasersedu/third_party.git

> cd ~/erasersedu_ws

> catkin_make

> source devel/setup.bash


* Install ROS libraries:

Ubuntu 16.04

> sudo apt-get install ros-kinetic-librealsense

> sudo apt-get install ros-kinetic-turtlebot

> sudo apt-get install ros-kinetic-turtlebot-apps

> sudo apt-get install ros-kinetic-turtlebot-interactions

> sudo apt-get install ros-kinetic-turtlebot-simulator

> sudo apt-get install ros-kinetic-ar-track-alvar-msgs


Ubuntu 18.04

> sudo apt-get install ros-melodic-kobuki-* -y

> sudo apt-get install ros-melodic-ecl-streams -y


In Ubuntu 18.04, if the following errors appear:

`/home/luis/erasersedu_ws/src/third_party/turtlebot/turtlebot_arm/turtlebot_arm_ikfast_plugin/src/turtlebot_arm_arm_ikfast_moveit_plugin.cpp:253:109: error: no matching function for call to ‘const_pointer_cast<urdf::Link>(urdf::LinkConstSharedPtr)’`

`~/erasersedu_ws/src/third_party/turtlebot/turtlebot_arm/turtlebot_arm_ikfast_plugin/src/turtlebot_arm_arm_ikfast_moveit_plugin.cpp:258:50: error: conversion from ‘urdf::JointSharedPtr {aka std::shared_ptr<urdf::Joint>}’ to non-scalar type ‘boost::shared_ptr<urdf::Joint>’ requested`

You need to change the word "boost" to "std" in lines 253 and 258 in the file "turtlebot_arm_arm_ikfast_moveit_plugin.cpp"
