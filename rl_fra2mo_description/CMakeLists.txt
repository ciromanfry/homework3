cmake_minimum_required(VERSION 3.5)
project(rl_fra2mo_description)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

# Trova le dipendenze
find_package(ament_cmake REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)
find_package(urdf REQUIRED)
find_package(xacro REQUIRED)
find_package(tf2 REQUIRED)
find_package(tf2_ros REQUIRED)

# Installa i file necessari
install(DIRECTORY launch urdf models meshes worlds
  DESTINATION share/${PROJECT_NAME}
)

ament_package()


