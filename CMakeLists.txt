cmake_minimum_required(VERSION 2.8.12)

project(MAVLink_connection)

if(NOT MSVC)
    add_definitions("-std=c++11 -Wall -Wextra -Werror")
else()
    add_definitions("-std=c++11 -WX -W2")
endif()

find_package(MAVSDK REQUIRED)

#find_library(wiringPi_LIB wiringPi)

add_executable(MAVLink_connection
    MAVLink_connection.cpp
)

target_link_libraries(MAVLink_connection
    MAVSDK::mavsdk_telemetry
    MAVSDK::mavsdk_action
    MAVSDK::mavsdk
    #wiringPi_LIB
)
