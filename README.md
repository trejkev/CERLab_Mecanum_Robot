# CERLab_Mecanum_Robot
Descriptor files for the CERLab Mecanum Robots, see: https://cerlab.ucr.ac.cr/es/node/202

The simulated robot looks just like the simulated robot shown in the following image, which is a shell replica of the CERLab Mecanum robots, see the second image for reference.

<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/af0eebfd-0583-43fe-911a-ac974938921e" width="600" />
</p>
<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/caf69869-f814-48b6-8b9d-1f3c3dfd50f8" width="600" />
</p>

<p align="center">
  <img src="https://github.com/trejkev/cerlab_mecanum/assets/18760154/2e21e592-5d20-4568-9c70-0cabc4dd2a3a" width="600" />
</p>

The robot is a functional replica of the CERLab platforms, it uses both LiDARs and has real mecanum movement, controlled by the gazebo plugin gazebo_mecanum_plugins, and use kinetic branch for ROS1 tests.

## Prerequisites:
1. Make sure you have everything needed to simulate with Gazebo. The robot was developed using Gazebo 9.
2. Make sure you have installed a ROS1 flavor of ROS. The robot was tested using ROS Melodic.
3. Make sure you have keyboard teleop installed for your ROS version. See http://wiki.ros.org/teleop_twist_keyboard
4. Make sure you have gazebo_mecanum_plugins cloned into catkin_ws, and switched to ros1-kinetic. See https://github.com/qaz9517532846/gazebo_mecanum_plugins.git

## To use the robot:
1. Clone this repo into catkin_ws.
3. Navigate to catkin_ws and execute catkin_make.
4. In a terminal execute roscore.
5. Once ROS core is up and running, in another terminal launch the robot with roslaunch cerlab_mecanum single_robot.launch, it will launch the robot in a Gazebo environment and also open Rviz configured to show the robot, its movement, and its sensors data.
6. At last, execute the teleoperation node to control the robot movement in an extra terminal, use rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/cerlab_mec_1/cmd_vel
