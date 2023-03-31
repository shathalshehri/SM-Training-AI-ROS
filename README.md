# SM Training: AI and Robotics First Task

 1.1 ROS Noetic on Ubuntu Installation (ROS-Noetic-on-Ubuntu-20)
How to Install ROS Noetic on Ubuntu 20.04 LTS
 
In this repository, I will show you how to Install ROS on Ubuntu operating system.  I’ve already installed Ubuntu 20.04.3 on Virtual Machine. So if you have not installed VirtualBox on your operating system yet, just install it (I’ll put the references that you will need down below) and then you will have to download Linux operating system like Ubuntu from their website, which you will be able to have its iso file that will be on top of the VirtualBox. 
1.         To install VirtualBox  https://www.virtualbox.org/wiki/Downloads  
2.         To install Ubuntu iso  https://ubuntu.com 
If there were any difficulties with the installation process I’d recommend that you follow up on the steps from a youtube video, just type your Operating system and what you would like to install on it, and if there are any errors, just copy and paste it on your browser, try to understand what is the problem and how to solve it.
 
First, what is ROS (Robotic Operating System)?
ROS stands for Robot Operating System more like an environment. It has the ability to connect nodes together, and by nodes, we mean pieces of software that can be written in C++ or Python. They can take care of a small subset of tasks such as: reading a sensor or controlling a servo. Those nodes connect together by a publisher/subscribe protocol. 
 
To Install ROS Noetic on Ubuntu 
Follow the steps below and write the commands on terminal
 
1.        Set up ROS Noetic repo for Ubuntu 20.04
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
 
2.        Add official ROS keyring
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
3.        Update ros package index
sudo apt update
      ￼
 
4.     Install ROS Noetic package 
In most cases, you will want to install ros-noetic-desktop-full for full ROS experience  (Recommended)
 
sudo apt install ros-noetic-desktop-full
￼
5.        Verify noetic installation
 
You must source this script in every bash terminal you use ROS in. 
source /opt/ros/noetic/setup.bash
then, write roscore to make sure that the installation process was successful
 
roscore 
￼
 
 

 1.2 ROS2 and Xubuntu on Jetson Nano Installation (Ubuntu&ROS2-in-JetsonNano)

