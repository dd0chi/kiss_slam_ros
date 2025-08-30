cmake_minimum_required(VERSION 3.0.2)
project(kiss_slam_ros)

# Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  geometry_msgs
  sensor_msgs
  nav_msgs
  tf
)

# Declare a catkin package
catkin_package(
  CATKIN_DEPENDS rospy std_msgs geometry_msgs sensor_msgs nav_msgs tf
)

# Install Python files	
catkin_install_python(PROGRAMS
  scripts/kiss_slam_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

# Install package.xml
install(
  FILES package.xml
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

# Install additional resources if necessary
install(
  DIRECTORY resource/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/resource
)
