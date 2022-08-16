# Slam_mapping
Step 1
$\ sudo apt-get install ros--joy ros-noetic-teleop-twist-joy 
$ \ ros-kinetic-teleop-twist-keyboard ros-noetic-laser-proc
$\ ros- kinetic -rgbd-launch ros-noetic-rosserial-arduino
$\ ros- kinetic -rosserial-python ros-noetic-rosserial-client
$\ ros- kinetic -rosserial-msgs ros-noetic-amcl ros-noetic-map-server
$\ ros- kinetic -move-base ros-noetic-urdf ros-noetic-xacro
$\ ros- kinetic -compressed-image-transport ros- kinetic -rqt* ros kinetic -rviz ros- kinetic -gmapping ros-noetic-navigation ros- kinetic -interactive-markers
sudo apt install ros- kinetic -hls-lfcd-lds-driver$ sudo apt install ros- kinetic -dynamixel-sdk $
step2
$ mkdir -p ~/catkin_ws/src $ cd catkin_ws/src$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3.get
$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations$
$ cd ~/catkin_ws &&catkin_make$
step3
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
step4
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
$ rosrun map_server map_saver -f ~/map 
