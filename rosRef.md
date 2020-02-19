## This repository contains some quick reference for ROS 

`Assuming you have a catkin workspace already created with folder name catkin_ws`

## Basic

### Sourcing the ros workspace.
If you have freshly created a workspace, every time you open a new terminal and try to run roscore you may face an error:
```shell
-bash: roscore: command not found
```
You need to source the catkin workspace with the following line of code
```shell
source catkin_ws/devel/setup.bash
```

### Creating your own package
We can create a new ros package in our catking workspace.
First we change the directory and then create the package
```shell
#Changing directory
cd ~/catkin_ws/src

# Creating the package
catkin_create_pkg cretus std_msgs rospy roscpp
#catkin_create_pkg <package_name> [depend1] [depend2] [depend3]

# build the package and catking workspace
cd ~/catkin_ws
catkin_make

# Souce the workspace after building the new package
source ~/catkin_ws/devel/setup.bash
```

### Exploring the files in a rospackage or ros workspace
```shell
# Get list of all the ros packages in your workspace with their location
rospack list

# you can directly `cd` to a perticular ros package
roscd cretus

# cd to the home directory
cd ~

# find a package directory using 
rospack find cretus 

# list all the components in a package
rosls cretus
```



















Some important links for ROS:
1 . http://wiki.ros.org/ROS/Tutorials
