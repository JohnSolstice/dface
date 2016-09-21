cmake_minimum_required(VERSION 3.6)
project(tester)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(tester ${SOURCE_FILES})

#dlib static library location
target_link_libraries(tester ${CMAKE_CURRENT_SOURCE_DIR}/../dlib/builds/Release/libdlib.a)

#dlib headers location
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../dlib)



include(${CMAKE_CURRENT_SOURCE_DIR}/../dlib/dlib/cmake)




