cmake_minimum_required(VERSION 3.5)
project(interface)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)

# Generate custom message
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/RemoteControlMessage.msg"
  "srv/MavServo.srv"
  DEPENDENCIES std_msgs
)

ament_package()