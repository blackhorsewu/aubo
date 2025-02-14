cmake_minimum_required(VERSION 3.0.2)
project(aubo_description)

# Find catkin and required packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  urdf
)

# Catkin package configuration
catkin_package(
  CATKIN_DEPENDS roscpp rospy std_msgs urdf
)

# Install URDF files
install(DIRECTORY
  urdf/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/urdf
)

# Install config files (if applicable)
install(DIRECTORY
  config/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config
)

# Install mesh files (if applicable)
install(DIRECTORY
  meshes/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/meshes
)
