# print-topics-using-ros1-bridge
To print topic from ros1 to ros2 using ros1_bridge, follow these steps:


## 1.	Make sure you Installed ROS 1 and ROS 2 and Set Up Your Workspace.
## 2.	Source the Environments:
Open a terminal and source both ROS distributions:

```
source /opt/ros/noetic/setup.bash  # For ROS 1
source /opt/ros/foxy/setup.bash    # For ROS 2
```
## 3.	Start ROS 1 Core:
In a new terminal, start the ROS 1 core:

```
roscore
```
## 4.	Publish a ROS 1 Topic:
In another terminal, publish a sample ROS 1 topic:

```
rostopic pub /ros1_topic std_msgs/String "data: 'Hello from ROS 1'"
```
## 5.	Run the ROS 1 Bridge:
In a new terminal, execute the ros1_bridge:

```
ros2 run ros1_bridge dynamic_bridge
```
## 6.	Subscribe to the Topic in ROS 2:
Open another terminal and subscribe to the corresponding ROS 2 topic:

```
ros2 topic echo /ros1_topic
```

## ros1_bridge has successfully established a connection between ROS 1 and ROS 2, now you can easily share data between the two systems.
