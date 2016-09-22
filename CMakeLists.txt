cmake_minimum_required(VERSION 2.8.4)
project(tester)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include(../dlib/dlib/cmake)

# compile main.cpp
add_executable(tester main.cpp)

# add dlib
target_link_libraries(tester dlib )

# add opencv
find_package(OpenCV REQUIRED)
target_link_libraries(tester ${OpenCV_LIBS})