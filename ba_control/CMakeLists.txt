cmake_minimum_required(VERSION 3.8)
project(ba_control)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)

set(dependencies
   rclcpp
   std_msgs
   sensor_msgs
)

# TODO 4 : add executable for the cpp file
# Your code here
# Your code here

install(TARGETS
   parse_and_publish
   ARCHIVE DESTINATION lib
   LIBRARY DESTINATION lib
   RUNTIME DESTINATION lib/${PROJECT_NAME}
)

install(
   DIRECTORY src launch
   DESTINATION share/${PROJECT_NAME}/
)

ament_package()
