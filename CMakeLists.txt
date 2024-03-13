cmake_minimum_required(VERSION 2.8.13)
project(camera_control_msgs)

find_package(catkin REQUIRED COMPONENTS 
actionlib_msgs
message_generation
sensor_msgs
)

add_action_files(DIRECTORY action)
add_service_files(DIRECTORY srv)

generate_messages(DEPENDENCIES 
actionlib_msgs
sensor_msgs
)

catkin_package(CATKIN_DEPENDS 
actionlib_msgs
message_runtime
sensor_msgs
)
