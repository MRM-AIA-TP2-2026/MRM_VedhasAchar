# Chatroom Using Ros2

## Description:
This is a project to implement a chatroom where any number of nodes can publish as well subscribe simultaneously.<br>
It is similar to whatsapp. Where a node is basically a person. 

## Approach:
First i created a Cmake package using `ros2 pkg create --build-type ament_cmake chatroom` and then inside it. i went into src using `cd src`<br>
then there i made a cpp file called `chat_node.cpp`. i wrote the c++ code into that. <br>
then i went back to my package dir, and updated the CMakeLists.txt file. Also updated my package.xml file to make those two execute my nodes.<br>
then i went to my ros2 workspace using `cd ~/Ros2_Workspace` then i built using `colcon build --packages-select chatroom` <br>
then, i sourced the code into my terminal using `source install/setup.bash` then i ran the package using 
`ros2 run chatroom chat_node A` in one of my terminal. then did the same steps in another one of my terminals. and did the same to another terminal.<br>
then when i typed anything on any of the terminals, it showed on other terminals.

## Message and Topic:
`/chatroom` is my topic<br>
`std_msgs/msg/String` is the Message data used

## RQT Graph:
![image](https://github.com/user-attachments/assets/6e522be0-1acf-41a2-8eca-3d358b9f9264)
