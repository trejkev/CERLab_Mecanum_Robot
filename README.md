# CERLab_Mecanum_Robot

Simulated version of the CERLab Mecanum Robots, see: https://cerlab.ucr.ac.cr/es/node/202

The simulated robot looks just like the real robot, see the first and second images, it is a shell replica of the CERLab Mecanum robots, see the third image for reference.

<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/bd5e0dfb-f88a-49bc-9b43-27bb6d70baef" width="600" />
</p>

<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/0bdda1b0-13c4-40d1-b4a0-db7eee90de76" width="600" />
</p>

<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/9b2c41c3-baca-416b-a209-c6814dc0385e" width="600" />
</p>


The robot is a functional replica of the CERLab platforms, it uses both LiDARs and has real mecanum movement, controlled by the gazebo plugin gazebo_mecanum_plugins.

## Prerequisites:
1. Make sure you have everything needed to simulate with Gazebo. The robot was developed using Gazebo 9.
2. Make sure you have installed a ROS1 flavor of ROS. The robot was tested using ROS Melodic.
3. Make sure you have keyboard teleop installed for your ROS version. See http://wiki.ros.org/teleop_twist_keyboard
4. Make sure you have gazebo_mecanum_plugins cloned into catkin_ws, and switched to ros1-kinetic. See https://github.com/qaz9517532846/gazebo_mecanum_plugins.git

## To use the robot:
1. Clone this repo into catkin_ws.
3. Navigate to catkin_ws and execute catkin_make.
4. In a terminal execute roscore.
5. Once ROS core is up and running, in another terminal launch the robot with the following command:

        roslaunch cerlab_mecanum single_robot.launch</span>

   It will launch the robot in a Gazebo environment and also open Rviz configured to show the robot, its movement, and its sensors data.
6. At last, execute the teleoperation node to control the robot movement in an extra terminal, use the following command:

       rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/cerlab_mec/cmd_vel

   It will allow you to use the teleoperation keyboard to control the robot.
