cmake_minimum_required(VERSION 2.8.3)
project(show_trajectory)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)


catkin_package(

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)


add_executable(by_marker src/marker.cpp)
target_link_libraries(by_marker ${catkin_LIBRARIES})

add_executable(by_marker_list src/marker_list.cpp)
target_link_libraries(by_marker_list ${catkin_LIBRARIES})

add_executable(by_path src/path.cpp)
target_link_libraries(by_path ${catkin_LIBRARIES})


