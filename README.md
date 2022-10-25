## Indoor Robot Simulation Environment 

This repo is to simulate the Indoor robot using Diff drive plug-in for Gazebo
The description file include multiple Macros for each of the following: 


1- Gazebo Control  
2- Robot description  
3- Inertial Macros  

---

The Environment have been created and was been saved as .world file 

---
#### Git Clone Repo
open terminal and create your workspace

```
mkdir dev_ws
cd dev_ws 
mkdir src
```
then after that git clone the repo 
```
git clone https://github.com/AElmaghawry/my_bot.git
```
---
#### Build Repo 
before your build make sure that your in the workspace 
```
cd ~/dev_ws/
```

build your project 

```
colcon build 
```

after that source the workspace 
```
. install/setup.bash
```
---

#### Launch Simulation 

open up 3 terminals

1. RVIZ terminal 

> If you want to launch RVIZ without any predefined configuration   
```
rviz2 
```
> if you created your own world you can call it as follows:
```
rviz2 -d src/my_bot/config/view_bot2.rviz
```

2. RUN Gazebo

>if you want to run the robot in empty environment 
~~~
ros2 (the Name of the package) (launch file)
~~~
type in as follow: 

```
ros2 launch my_bot launch_sim.launch.py  
```
>if you have your own saved world file you can type: 

```
ros2 launch my_bot launch_sim.launch.py world:=./src/my_bot/worlds/obstecales.world 
```
3. Use Teleop Commands to control the robot 

```
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```


