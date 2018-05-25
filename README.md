# Introduction
This repository collected 3 ways to show trajectory of robot in ROS. And I had test them all in indigo.
# How to Run
There are three nodes declared in CMakeLists.txt. You just need to
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
<br>and then add corresponding display in rviz
<br>![](http://wiki.ros.org/rviz/UserGuide?action=AttachFile&do=get&target=add_display_button.png)
<br>by_path add **Path**
<br>by_marker and by_marker_list add **Marker**

# Three Ways
## 1. nav_msgs/Path
public a [nav_msgs::Path](http://docs.ros.org/api/nav_msgs/html/msg/Path.html) message which contains an array of geometry_msgs/PoseStamped
<br>![result](https://img-blog.csdn.net/20180525160856852?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM4MzQ1MjU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
## 2. visualization_msgs/Marker
public [visualization_msgs::Marker](http://wiki.ros.org/rviz/Tutorials/Markers%3A%20Basic%20Shapes) and hold them by setting **lifetime** to forever. But remember to update the **id** of Marker to avoid covering previous markers.
<br>![result](https://img-blog.csdn.net/20180525152435566?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM4MzQ1MjU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
## 3. visualization_msgs/Marker list
public [visualization_msgs::Marker's points and lines](http://wiki.ros.org/rviz/Tutorials/Markers%3A%20Points%20and%20Lines) which contains an array of geometry_msgs/Point
<br>![result](https://img-blog.csdn.net/20180525152613816?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM4MzQ1MjU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

<br>Thank you for your star!(grinning)
