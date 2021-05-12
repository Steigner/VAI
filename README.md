### Artificial Intelligence Algorithms
This repository contain very simple approach of appliacation and comparation A* and RRT algorithm for path planning cobot UR3 from Universal Robots.

**Course aims**: The course objective is to make students familiar with basic resources of artificial intelligence, potential and adequacy of their use in engineering problems solving.

For application was used:
* OS Ubuntu 18.04
* ROS Melodic
* Moveit 1
* Python 2 -> with added library Plotly

Repository contain 2 folders:

* path_planning - this ros package integrate to your catkin workaspace
* technical_report - folder contain technical report for this project in [[czech lang.]](https://en.wikipedia.org/wiki/Czech_language).

### Note
Algorithms wasn't programmed in the most elegantly way. Main reason is attempt to avoid common solutions.
Time of finding solution is horrible, so in conclusion for real world application is better use modification of standalone algorithms as BiRRT etc... or programmed it in C++ or some faster prog. language alternativly Julia.

### How to run?
#### Install dependencies
* [ROS] http://wiki.ros.org/melodic/Installation/Ubuntu
* [MOVEIT] https://moveit.ros.org/install/
* [ROS Universal Robot] https://github.com/ros-industrial/universal_robot.git
* [Universal Robots ROS Driver] https://github.com/UniversalRobots/Universal_Robots_ROS_Driver
#### Simulation in Gazebo
*  user@user-pc:~$ roslaunch ur_gazebo ur3.launch
*  user@user-pc:~$ roslaunch ur3_moveit_config ur3_moveit_planning_execution.launch sim:=true
*  user@user-pc:~$ roslaunch ur3_moveit_config moveit_rviz.launch
*  user@user-pc:~$ rosrun path_planning run.py

#### Real Robot
*  user@user-pc:~$ roslaunch ur_robot_driver ur3_bringup.launch robot_ip:=xxx.xxx.xxx.xxx
*  user@user-pc:~$ roslaunch ur3_moveit_config ur3_moveit_planning_execution.launch
*  user@user-pc:~$ roslaunch ur3_moveit_config moveit_rviz.launch
*  user@user-pc:~$ rosrun path_planning run.py

### References
* [Faculty of Mechanical Engineering BUT](https://www.fme.vutbr.cz/en)
