cmake_minimum_required(VERSION 2.8)
project(sick_lms400)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

cs_add_library(${PROJECT_NAME} src/sick_lms400.cpp)

cs_add_executable(lms400_node src/lms400_node.cpp)
target_link_libraries(lms400_node ${PROJECT_NAME})

cs_install()
cs_export()

