# ROS_Simulation

ติดตั้งเครื่องมือที่จำเป็น ก่อนการ Simulation

      $ sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc ros-noetic-rgbd-launch ros-noetic-depthimage-to-laserscan ros-noetic-rosserial-arduino ros-noetic-rosserial-python ros-noetic-rosserial-server ros-noetic-rosserial-client ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro ros-noetic-compressed-image-transport ros-noetic-rqt-image-view ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers 
      
      
ติดตั้ง TurtleBot

      $ cd ~/catkin_ws/src/
      
      $ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
      
      $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git 
      
      $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git 
      
      $ cd ~/catkin_ws 
      
      $ catkin_make 
      
เปิด Bot ใน Gazebo

      $ export TURTLEBOT3_MODEL=burger
      
      $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
      
เปิดรีโมท teleop_key
      
      $ export TURTLEBOT3_MODEL=burger

      $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
      
      
เปิด SLAM

      $ export TURTLEBOT3_MODEL=burger
      
      $ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
      
      ในกรณีต้องการ Save Map 
      
      $ rosrun map_server map_saver -f ~/map
      
      
      
