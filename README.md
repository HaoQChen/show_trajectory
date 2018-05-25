# Introduction
This repository collected 3 ways to show trajectory of robot in ROS. And I had test them all in indigo.
# How to Run
There are three node declared in CMakeLists.txt. You just need to
```
catkin_make
roscore
rosrun rviz rviz
rosrun show_trajectory by_path
or
rosrun show_trajectory by_marker
or
rosrun show_trajectory by_marker_list
```
and then add corresponding display in rviz
<br>![](http://wiki.ros.org/rviz/UserGuide?action=AttachFile&do=get&target=add_display_button.png)
<br>by_path add **Path**
<br>by_marker and by_marker_list add **Marker**

# Three Ways
## nav_msgs/Path
public a nav_msgs::Path message which contains an array of geometry_msgs/PoseStamped
## visualization_msgs/Marker
public [visualization_msgs::Marker](http://wiki.ros.org/rviz/Tutorials/Markers%3A%20Basic%20Shapes) and hold them by setting **lifetime** to forever. But remember to update the **id** of Marker to avoid covering previous markers.
## visualization_msgs/Marker list
public [visualization_msgs::Marker's points and lines](http://wiki.ros.org/rviz/Tutorials/Markers%3A%20Points%20and%20Lines)


