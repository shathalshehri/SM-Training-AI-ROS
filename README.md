# SM Training: AI and Robotics First Task

 ## 1.1 ROS Noetic on Ubuntu Installation (ROS-Noetic-on-Ubuntu-20)
  
  **How to Install ROS Noetic on Ubuntu 20.04 LTS**

In this section, I will show you how to Install ROS on Ubuntu operating system.  I’ve already installed Ubuntu 20.04.3 on Virtual Machine. So if you have not installed VirtualBox on your operating system yet, just install it (I’ll put the references that you will need down below) and then you will have to download Linux operating system like Ubuntu from their website, which you will be able to have its iso file that will be on top of the VirtualBox. 

**1.	To install VirtualBox**  https://www.virtualbox.org/wiki/Downloads  
**2.	To install Ubuntu iso**  https://ubuntu.com 

If there were any difficulties with the installation process I’d recommend that you follow up on the steps from a youtube video, just type your Operating system and what you would like to install on it, and if there are any errors, just copy and paste it on your browser, try to understand what is the problem and how to solve it.

First, what is ROS (Robotic Operating System)?

ROS stands for Robot Operating System more like an environment. It has the ability to connect nodes together, and by nodes, we mean pieces of software that can be written in C++ or Python. They can take care of a small subset of tasks such as: reading a sensor or controlling a servo. Those nodes connect together by a publisher/subscribe protocol. 

To Install ROS Noetic on Ubuntu 

Follow the steps below and write the commands on terminal

**1.	Set up ROS Noetic repo for Ubuntu 20.04**
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
``` 

**2.	Add official ROS keyring**
```
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
**3.	Update ros package index**
```
sudo apt update
```

![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img1.png)

**4.	Install ROS Noetic package** 

In most cases, you will want to install ros-noetic-desktop-full for full ROS experience  (Recommended)

```
sudo apt install ros-noetic-desktop-full
```

![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img2.png)

**5.	Verify noetic installation**

You must source this script in every bash terminal you use ROS in. 
```
source /opt/ros/noetic/setup.bash
```

then, write roscore to make sure that the installation process was successful

```
roscore 
```
![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img3.png)

 ## 1.2 ROS2 and Xubuntu on Jetson Nano Installation (Ubuntu&ROS2-in-JetsonNano)

**How to install Ubuntu and ROS2 in Jetson Nano**

•	Install xubuntu in Jetson Nano

In this section I will show how to install Ubuntu & ROS2 on a Jetson Nano
We will download (Xubuntu 20.04 Focal Fossa L4T R32.3.1) instead of Ubuntu because it is a custom image for the Jetson Nano



**1.	Open** ( https://forums.developer.nvidia.com/t/xubuntu-20-04-focal-fossa-l4t-r32-3-1-custom-image-for-the-jetson-nano/121768) 
**2.	Click on the download link :** Xubuntu-20.04-l4t-32.3.1.tar.tbz2 

 ![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img4.png)
 
 **3.	After the following window pops up, click on Save file>OK **
 
 ![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img5.png)
 
## •	Download balena

**1.	You need to flash your SD card using balenaEtcher (Recommended) , here is the link that will do that for you: https://www.balena.io/etcher/ , click Download for Linux x64 > Save File> OK**

![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img6.png)

**2.	Click on Extract Here so you can have the app image**
![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img7.png) ![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img8.png)

**3.	Now  the program is set up**
![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img9.png)

**4.	Before you can flash the image you have to Extract the zip file for ubuntu that you’ve download it using the Terminal type this command to extract the Xubuntu image:**

tar -xvjf Xubuntu-20.04-l4t-r32.3.1.tar.tbz2

![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img10.png)

**5.	Go back to the balena Etcher > Flash from file> Downloads>Xubuntu-20.04…. (Select the image for xubuntu)**
![alt text](https://github.com/shathalshehri/SM-Training-AI-ROS/blob/main/img11.png)








