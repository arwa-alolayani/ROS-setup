# ROS-setup
Guide to setup ROS on Ubuntu using VirtualBox
##  Prerequisites
* VirtualBox 6.1.36
* Ubuntu 20.04.4 64bit
* ROS kinetic 
## Steps
1. [install VirtualBox]  
2. [Create a new Virtual Machine] 
3. [Configurating the VirtualMachine]
4. [Install Ubuntu]
5. [Installing ROS on Ubuntu]

## install VirtualBox
1- Go to www.virtualbox.org and download the newest version of VirtualBox 

2- Install VirtualBox

## Create a new Virtual Machine 

1- Run VirtualBox and create a new VM (Virtual Machine) by clicking New  

2- Name the new VM - Ubuntu (version), choose 'Linux' for the operating system and “Ubuntu (64-bit)” for the boot version, then > click Next 
![image](https://user-images.githubusercontent.com/90524059/180397656-b1a131ab-7ab4-479a-a085-464af3ea2c44.png)

3- Allocate RAM for Guest OS - preferable half the size of RAM you have on your PC, then > click Next 

4-  Create a Virtual Hard Disk, then select VDI > click Next, configurating the Type of VD (Virtual Disk) > select Fixed size storage > click Next, choosing the file location and size 

![image](https://user-images.githubusercontent.com/90524059/180401921-d9a67646-ff77-48a3-a41e-5ea9465d61a2.png)

5- Click Create the Virtual Machine 

## Configurating the VirtualMachine
1- Right-click on the newly created virtual machine and click Settings. 

2- Navigate to Storage on the left-hand menu and select the Storage tab. Click on the line with the CD. On the right, under Optical Drive > click on the CD icon with the down arrow and select Choose a disk file > the earlier downloaded Ubuntu ISO.

3- choose System on the left-hand menu and select the Processor tab. Increase the slider until the end of the green zone, which may be different for each PC > click OK


## Install Ubuntu
1- Download Ubuntu ISO from https://ubuntu.com/download/desktop

2- Double click on the newly created virtual machine.

3- Wait while the virtual machine to checks the disk.

4- Select Install Ubuntu, the choose your keyboard layout as English > click Continue.

5- Select Minimal installation, Download updates while installing Ubuntu and Install third-party software for graphics and Wi-Fi hardware and additional media formats > Click Continue

6- Select Erase disk and install Ubuntu then > Click Install Now and click Continue if a warning pops out.

7- Next you have to select your country and personal information > click Continue and whait while Ubuntu installs
![image](https://user-images.githubusercontent.com/90524059/180408180-70b86434-580d-4ffb-81e5-4b9a9d6b379a.png)


## Installing ROS on Ubuntu
To install ROS on Ubuntu the instractions found on http://wiki.ros.org/noetic/Installation/Ubuntu will be followed 
1- Open Software & Updates

### 1. Setup your sources.list
Setup your computer to accept software from packages.ros.org.

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

### 2. Set up your keys
```
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

### 3. Installation
```
sudo apt update
```

### 4 Desktop-Full Install:
```
sudo apt install ros-noetic-desktop-full
```

### 5. Environment setup
```
source /opt/ros/noetic/setup.bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
gedit~/.bashrc
```
With these commands, Rose was downloaded successfully. To make sure, we type the command:
```
roscore
```
