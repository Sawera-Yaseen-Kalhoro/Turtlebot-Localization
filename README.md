# Turtlebot Localization Package

This package contains some nodes to localize a turtlebot with EKF, using wheel encoders for Prediction and yaw reading from IMU magnetometer for Update.

## Contents

This package contains:

* `localization_node.py`: node to localize a turtlebot with EKF, using wheel encoders for Prediction and yaw reading from IMU magnetometer for Update.

* `twist_to_wheel_vel_node.py`: node to convert Twist into wheel velocities to control the turtlebot.

## Running the Package

This package is meant to run inside the turtlebot through ssh. Thus, copy this package into the workspace inside the turtlebot using SFTP. Then, run `kobuki_mobile_base.launch` and `kobuki_sensors.launch` in the `turtlebot` package through ssh. Finally, source the workspace and run the following command in the terminal (through ssh):

```bash
roslaunch turtlebot_localization localization_controller.launch
```

This launch file will run all nodes in this package.

## Extra: Teleop

A nice teleop interface can be launched by typing this command line in the terminal:

```bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py 
```

To run this, you need to have `teleop_twist_keyboard` installed. To install it, simply run

```bash
sudo apt-get install ros-noetic-teleop-twist-keyboard
```

For more information, refer to this [link](https://wiki.ros.org/teleop_twist_keyboard).