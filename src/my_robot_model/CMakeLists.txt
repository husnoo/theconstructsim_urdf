cmake_minimum_required(VERSION 3.8)
project(my_robot_model)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)
find_package(xacro REQUIRED)
find_package(gazebo_ros REQUIRED)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

install(
  DIRECTORY
    urdf
    rviz
    launch
    meshes
	worlds
    models
  DESTINATION
    share/${PROJECT_NAME}/
)

find_package(ament_cmake REQUIRED)
find_package(rclpy REQUIRED)

ament_package()