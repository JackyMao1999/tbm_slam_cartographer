# tbm_slam_cartographer
tianbot_mini cartographer功能包


tbm_slam_cartographer 是为TianbotMini ROS移动机器人学习平台专门搭建的建图算法功能包。

# 使用指南

## 创建工作空间 tianbot_mini_ws

mkdir tianbot_mini_ws/src -p  
cd ~/tianbot_mini_ws/src  

## 部署 tianbot_mini_zoo功能包

cd ~/tianbot_mini_ws/src  
git clone https://github.com/tianbot/tianbot_mini.git  

## 部署tbm_slam_cartographer功能包

cd ~/tianbot_mini_ws/src 

git clone https://github.com/tianbot/tianbot_mini.git  

## 编译工作空间 tianbot_mini_ws

source /opt/ros/melodic/setup.bash  
cd ~/tianbot_mini_ws/  
catkin_make  
echo "source ~/tianbot_mini_ws/devel/setup.bash --extend" >> ~/.bashrc  



|      |      |
| ---- | ---- |
|      |      |
|      |      |
|      |      |





锡城筱凯 备 2021.05.30
