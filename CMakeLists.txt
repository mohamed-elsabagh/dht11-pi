cmake_minimum_required(VERSION 3.7.2)
project(dht11-pi)

find_package(Threads REQUIRED)

set(APP_NAME "kaa-pi")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c99 -g -Wall -Wextra")

set(SOURCE_FILES
    dht11.c)

include_directories(${INCLUDE_DIRECTORIES})

add_executable(${APP_NAME} ${SOURCE_FILES})

target_link_libraries(${APP_NAME} wiringPi ${CMAKE_THREAD_LIBS_INIT})
