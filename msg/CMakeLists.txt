add_ros_message_files(io_mocap_msgs
  SPACE io_mocap
  FILES
    bend.msg
    touch.msg
    old_touch.msg
    mocap_data.msg
    squashed_mocap_data.msg
    squashed_bend.msg
    squashed_touch.msg
  DEPS
    std_msgs
    sensor_msgs
)
