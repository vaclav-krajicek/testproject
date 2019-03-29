cmake_minimum_required(VERSION 3.1.0)

project(testproject)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt5Widgets CONFIG REQUIRED)

set(testproject_SRCS
    openglwindow.h
    openglwindow.cpp
    main.cpp
)

add_executable(testproject WIN32 ${testproject_SRCS})
target_link_libraries(testproject Qt5::Widgets)
