this file will help you walk through how to install arudino robot arm package and what commands to write in order to install and open the arm depandacies such as gazeboo, moveit and RViz, there is also a tuturoial on how to install arduino inside ubuntu and install rosserial and ros_lib library.

# install_arduino_robot_Arm
#### 1- first thing we need to do is install catkin:

$ sudo apt-get install ros-noetic-catkin


#### 2- then change the dict to catkin's source by typing the following commands

$ mkdir -p ~/catkin_ws/src

$ cd ~/catkin_ws/

$ catkin_make

![image](https://user-images.githubusercontent.com/79508459/180758330-331c5240-8b89-481f-bd17-942479264758.png)



#### 3- type the following commands, to install git and conncet to github repostary

$ cd ~/catkin_ws/src

$ sudo apt install git

$ git clone https://github.com/smart-methods/arduino_robot_arm

$ cd ~/catkin_ws

![image](https://user-images.githubusercontent.com/79508459/180746458-c51c106b-3444-4197-a9be-ade4ce506c9b.png)


#### 4- install and initilzie rosdep 

$ sudo apt install python3-rosdep2

$ rosdep install --from-paths src --ignore-src -r -y

![image](https://user-images.githubusercontent.com/79508459/180747967-dbb6ea96-2ef0-4dd7-b77b-78b96f527ab9.png)

![image](https://user-images.githubusercontent.com/79508459/180748010-ddff3d2f-35ba-4e57-86f1-3fce91add969.png)

#### 5- install depandacies 

$ sudo apt-get install ros-noetic-moveit

$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

![image](https://user-images.githubusercontent.com/79508459/180748457-6cda236d-a091-4ff3-bb96-856893490b6f.png)

![image](https://user-images.githubusercontent.com/79508459/180748983-222f620c-2242-4782-bc8c-d1e3443f8664.png)

![image](https://user-images.githubusercontent.com/79508459/180749695-58c957af-3ae5-435d-b6f5-b987d4011ff0.png)

![image](https://user-images.githubusercontent.com/79508459/180749907-3ec039fd-2c8c-4b4b-a414-19a608159988.png)


#### 6- after installing the depandanices type the following command 

$ sudo nano ~/.bashrc

then go to the button and add the following line under the other sources

*note instead of 'faiza' write your user name

source /home/faiza/catkin_ws/devel/setup.bash

![image](https://user-images.githubusercontent.com/79508459/180750434-73e968a7-dc07-4d79-aa40-4b39f8d1b6b2.png)

![image](https://user-images.githubusercontent.com/79508459/180750465-783b85cc-9d47-4960-9c4b-582836f806c3.png)


####7 - type the following command to launch RViz

$ sudo roslaunch robot_Arm_pkg check_motors.launch 

![image](https://user-images.githubusercontent.com/79508459/180750761-c435f96e-2eed-47e6-a5a4-6d09c02b96f8.png)

![image](https://user-images.githubusercontent.com/79508459/180750775-8c6c9c65-7df6-4ce1-82c6-ff1a217d9fb7.png)

####8- type the fololowing command to lanuch gazebo

$roslaunch robot_Arm_pkg check motors_gazebo.launch

![image](https://user-images.githubusercontent.com/79508459/180751158-b58dcd5c-3107-42c9-818b-674565e0d60b.png)




# install arduino on ubuntu 

1- type the following commands 

$ sudo apt update

$ mkdir arduino

$ cd arduino/

$ wget https://downloads.arduino.cc/arduino-1.8.15-linux64.tar.xz

![image](https://user-images.githubusercontent.com/79508459/180752772-7b87e111-bf7b-456d-be85-10b6a8eba65a.png)

$ cd arduino-1.8.15/

$ sudo ./install.sh

![image](https://user-images.githubusercontent.com/79508459/180752963-03084099-2040-47b1-ab5f-c17305e9a77e.png)




## install rosserial

$ sudo apt-get install ros-noetic-rosserial-arduino

$ sudo apt-get install ros-noetic-rosserial

![image](https://user-images.githubusercontent.com/79508459/180753172-6c2f9555-8ee2-4585-af80-9fc58aa2ad8e.png)

![image](https://user-images.githubusercontent.com/79508459/180753251-e90eb434-0409-4a49-b783-ecd435fb5256.png)




## install ros_lib

go the arduino file and click right and chose open with terminal 

and then start typing the following commands

$ cd libraries

$ rosrun rosserial_arduino make_libraries.py

![image](https://user-images.githubusercontent.com/79508459/180753594-bcea3688-36c1-42aa-8129-bb5f2a1e4af8.png)



