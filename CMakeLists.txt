cmake_minimum_required(VERSION 3.6)
project(tester)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# add dlib
include(../dlib/dlib/cmake)

# compile main.cpp
add_executable(tester main.cpp)

# link dlib
TARGET_LINK_LIBRARIES(tester dlib )
