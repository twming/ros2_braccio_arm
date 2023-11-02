cmake_minimum_required(VERSION 3.8)
project(talk_listen)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

# TODO 7: add the talker.cpp file to compile

ament_target_dependencies(talker rclcpp std_msgs)

# TODO 7: add the listener.cpp file to compile

ament_target_dependencies(listener rclcpp std_msgs)

install(TARGETS
  talker
  listener
  DESTINATION lib/${PROJECT_NAME})


ament_package()
