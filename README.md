# Controller Workspace

A ROS interface for robot controllers bringup for marslite robot.

## Instructions

### Cartesian controllers

+ Bringup marslite with `cartesian_motion_controller`:
  ```bash
  roslaunch controller_bringup motion_controller_bringup.launch 
  ```
+ Bringup marslite with `cartesian_force_controller`:
  ```bash
  roslaunch controller_bringup force_controller_bringup.launch 
  ```
+ Bringup marslite with `cartesian_compliance_controller`:
  ```bash
  roslaunch controller_bringup compliance_controller_bringup.launch 
  ```
<!-- + Teleoperate the robotic arm with `cartesian_motion_controller` using keyboard inputs:
  ```bash
  ``` -->

**[Tips] To increase the motion speed of robotic arm, increase the value of `error_scale` in `controller_bringup/config/marslite_controllers.yaml`**

[Note] `cartesian_controllers`-related packages depend on `tm_driver` in current ROS workspace rather than that under `/opt/ros/kinetic/share` directory (which I don't know why). **DO NOT remove `tm_driver` from the workspace.**