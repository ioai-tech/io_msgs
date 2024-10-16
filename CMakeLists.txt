cmake_minimum_required(VERSION 3.0.2)
project(io_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  sensor_msgs
  geometry_msgs
  std_msgs)

add_message_files(FILES
  bend.msg
  claws_angle.msg
  imu_state.msg
  mocap_data.msg
  old_touch.msg
  squashed_bend.msg
  squashed_imu_state.msg
  squashed_mocap_data.msg
  squashed_touch.msg
  teleop_robot_state.msg
  robot_status.msg
  robot_expect_motion.msg
  io_tf_frame.msg
  io_pose.msg
  io_tf.msg
  touch.msg)

set(SERVICE_FILES
  SetRecord.srv
)

add_service_files(FILES ${SERVICE_FILES})

generate_messages(DEPENDENCIES std_msgs sensor_msgs geometry_msgs)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  sensor_msgs
  geometry_msgs
  std_msgs
  geometry_msgs
)
