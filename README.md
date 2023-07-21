# robot-arm-ROS
## Requirements

Oracle VM VirtualBox Manager version 7.0

Ubuntu-18.04.6-desktop-amd64.iso

ROS melodic <br/>
##

## Oracle VM VirtualBox


![Oracle VM VirtualBox Manager 7_21_2023 10_05_50 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/b8fc3e35-5966-407d-aa62-c023416ff3f8)

## Ubuntu-18.04.6


![safiya0  Running  - Oracle VM VirtualBox _ 1 7_16_2023 10_06_05 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/6a499eff-7be5-4985-b34f-ba8dec587854)

## Install ROS melodic 

![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 10_21_28 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/707ca029-ad52-4628-b1eb-5ac99b2d87a0)

![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 10_22_56 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/6ac577a3-1f78-4309-a914-83e286788c1a)

![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 10_23_44 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/ecb0d5f5-4119-414a-b5cb-e64721e68bc5)

*To download ROS melodic the copy commands and put them in your linux terminal.*


![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 10_28_18 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/34248b3d-c3fe-4127-9bef-94f8f5a29086)
##


## Create a workspace by using catkin_make
*Copy commands and put them in your linux terminal after downloaded ROS.*

```linux
$source / opt/ros/melodic/setup/bash
```

```linux
$mkdir -p ~/catkin_ws/src
$cd ~/catkin_ws/
$catkin_make
```

```linux
$echo "source ~/catkin_ws/devel/setup.bash" ~/.bashrc
```
##

## Install package robot arm 
*To download package robot arm the copy commands and put them in your linux terminal after create source catkin_ws*

```linux
$ cd ~/catkin_ws/src
$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm 
```
![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 10_50_57 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/a5ea2d98-0062-4da4-a60e-faf5b58eb928)


*add all the dependencies.*

```linux
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
```

*compile the package*

```linux
$ catkin_make
```
![safiya0  Running  - Oracle VM VirtualBox _ 1 7_16_2023 12_18_43 AM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/1ee6227d-4871-41d6-81e2-2221cebb8a76)


*Controlling the motors*

```linux
$ roslaunch robot_arm_pkg check_motors.launch
```

![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 11_12_20 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/21e89924-9ce3-42a0-a1ae-58195a994001)
##

## joint-state-publisher

![safiya0  Running  - Oracle VM VirtualBox _ 1 7_21_2023 11_19_16 PM](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/b656943e-6c90-4243-9746-498fb81fff45)


![WhatsApp Image 2023-07-21 at 23 30 04](https://github.com/SafiyaAli84/robot-arm-ROS/assets/140127999/d5c3dbf5-2a88-4057-9a6b-dd2ba1e9e95f)

base_joint = -0.89

shulder = 0.32

elbow = -0.52

wrist = -1.28

degree of rotation from -1.57 to 1.57












































