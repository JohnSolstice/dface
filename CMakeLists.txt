cmake_minimum_required(VERSION 3.6)
project(tester)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# compile main.cpp
add_executable(tester main.cpp)

# add dlib
#include(../dlib/dlib/cmake)
#target_link_libraries(tester dlib )
find_package(dlib REQUIRED)
target_link_libraries(tester dlib)

# add opencv
find_package(OpenCV REQUIRED)
target_link_libraries(tester ${OpenCV_LIBS})