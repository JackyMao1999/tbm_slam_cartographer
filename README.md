# tbm_slam_cartographer
tianbot_mini cartographer功能包


tbm_slam_cartographer 是为TianbotMini ROS移动机器人学习平台专门搭建的建图算法功能包。

# 使用指南

## 创建工作空间 tianbot_mini_ws

$ mkdir tianbot_mini_ws/src -p 

$ cd ~/tianbot_mini_ws/src  

## 部署 tianbot_mini_zoo功能包

$ cd ~/tianbot_mini_ws/src 

$ git clone https://github.com/tianbot/tianbot_mini.git  

## 部署tbm_slam_cartographer功能包

$ cd ~/tianbot_mini_ws/src 

$ git clone https://github.com/JackyMao1999/tbm_slam_cartographer.git

## 编译工作空间 tianbot_mini_ws

$ source /opt/ros/melodic/setup.bash 

$ cd ~/tianbot_mini_ws/ 

$ catkin_make 

$ echo "source ~/tianbot_mini_ws/devel/setup.bash --extend" >> ~/.bashrc  



## 使用方法

1. 为了使用Cartographer算法，通过串口连接Tianbot_mini，并且输入usetf 0，看到串口回复OK，重启机器人。
2. 使用tbm_slam_cartographer功能包一键运行cartographer建图。

## Launch文件

|           launch文件            |                             功能                             |
| :-----------------------------: | :----------------------------------------------------------: |
|     demo_slam_laser.launch      | **cartographer**算法使用**纯激光**建图，使用**MoveBase**路径规划算法 |
|   demo_slam_laser_odom.launch   | **cartographer**算法融合**激光**和**里程计**建图，使用**MoveBase**路径规划算法 |
| demo_slam_laser_odom_teb.launch | **cartographer**算法融合**激光**和**里程计**建图，使用**TEB**路径规划算法 |
|   demo_slam_laser_teb.launch    | **cartographer**算法使用**纯激光**建图，使用**TEB**路径规划算法 |



## 笔者测试该功能包遇到的问题及解决方法：

1. 有时出现地图漂移，重启机器人即可
2. 机器人无法导航，重启机器人即可
3. 机器人无法加载地图，可能是tf坐标转换错误，打开串口使用usetf 0命令，然后重启机器人。



锡城筱凯 备 2021.05.30
