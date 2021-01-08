cmake_minimum_required(VERSION 2.8)

project(autobahn-cpp)

find_package(catkin REQUIRED)

catkin_package(
  INCLUDE_DIRS
    ${CMAKE_CURRENT_SOURCE_DIR}
)

include(${CMAKE_CURRENT_SOURCE_DIR}/cmake/Includes/CMakeLists.txt)

option(AUTOBAHN_BUILD_EXAMPLES "Build examples" OFF)

if(AUTOBAHN_BUILD_EXAMPLES)
    add_subdirectory(examples)
endif(AUTOBAHN_BUILD_EXAMPLES)
