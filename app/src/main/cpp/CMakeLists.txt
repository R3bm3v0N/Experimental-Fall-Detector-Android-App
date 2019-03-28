cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Werror")

include_directories(src/main/cpp/detector/)

add_library(detector SHARED detector/detector.c)

target_link_libraries(
    detector
    android
    GLESv2
    log
)

