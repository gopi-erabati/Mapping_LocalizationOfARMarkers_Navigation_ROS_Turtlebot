# Mapping_LocalizationOfARMarkers_Navigation_ROS_Turtlebot

This Repository deals with the code for the project on "Mapping , Localizing AR Markers and navigation of Turtlebot using ROS".

The report for the project is added as a doc file, which includes the problem statement, strategy employed, packages used.

**Steps to run the code:**

**Real Time**

1. Connect to turtlebot from the workstation

`ssh turtlebot@ipaddress`

2. Bringup the robot, run the following *on the turtlebot*

`roslaunch turtlebot_bringup minimal.launch`

3. Mapping the environment using turtlebot, run the below code *on the turtlebot*

`roslaunch turtlebot_navigation gmapping_demo.launch`

4. Launch rviz to view the map, run the below code *on the workstation*

`roslaunch turtlebot_rviz_launchers view_navigation.launch`

5. Teleoperation to move the robot, run the below code *on the workstation*

`roslaunch turtlebot_teleop logitech_teleop.launch`

6. Navigate around the world and build the map

7. After complete mapping, save the map using below code , run *on the turtlkebot*

`rosrun map_server map_saver -f /tmp/my_map`

8. Change the amcl_demo launch file in turtlebot_navigation package on turtlebot, make the boolean values of registration, processing set to True.

9. Start amcl_demo , run the follwoing code *on the turtlebot*

`roslaunch turtlebot_bringup minimal.launch` (If minimal is not launched earlier)

`roslaunch turtlebot_navigation amcl_demo.launch map_file:=/path_to_your_map_file`

10. Run the nodes by launching a alltask launch file, run the below code *on the workstation*

`roslaunch Robo_Project alltask.launch`

