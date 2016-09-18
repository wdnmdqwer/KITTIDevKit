cmake_minimum_required(VERSION 3.5)
project(devkit)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(CMAKE_BUILD_TYPE Debug)

set(devkit_SRC_DIR ${PROJECT_SOURCE_DIR}/cpp)

FILE(GLOB devkit_SRC_FILES "cpp/*.cpp")


include_directories(${devkit_SRC_DIR})


set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)

add_executable(devkit ${devkit_SRC_FILES})
