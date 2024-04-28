cmake_minimum_required(VERSION 3.0.2)
project(io_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  sensor_msgs
  std_msgs)

add_message_files(FILES
  bend.msg
  touch.msg
  old_touch.msg
  mocap_data.msg
  squashed_mocap_data.msg
  squashed_bend.msg
  squashed_touch.msg)

generate_messages(DEPENDENCIES std_msgs sensor_msgs)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  sensor_msgs
  std_msgs
)
