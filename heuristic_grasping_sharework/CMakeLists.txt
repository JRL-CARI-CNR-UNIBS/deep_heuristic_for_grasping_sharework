cmake_minimum_required(VERSION 3.0.2)
project(heuristic_grasping_sharework)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  rospy
  std_msgs
  std_srvs
  message_generation
  message_runtime
)

add_message_files(
  FILES
  CustomBox.msg
  Feasibility.msg
)

add_service_files(
  FILES
  EstimateObjectsFeasibility.srv
)

generate_messages(
 DEPENDENCIES
 geometry_msgs   std_msgs
)

catkin_package(
  INCLUDE_DIRS
  LIBRARIES
  CATKIN_DEPENDS geometry_msgs rospy std_msgs std_srvs message_generation message_runtime
  DEPENDS
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
