cmake_minimum_required(VERSION 3.5)

project(sandsmark-screenshot LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_executable(screenshot main.cpp Widget.cpp)
target_link_libraries(screenshot PRIVATE Qt5::Widgets)

install(TARGETS screenshot DESTINATION bin)
