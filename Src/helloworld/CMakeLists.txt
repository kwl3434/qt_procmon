#CMake Project name

#add_executable()    source file
#add_library()       library
#add_subdirectory()  directory path
#add_dependencies() dependencies


cmake_minimum_required(VERSION 3.1.0)

project(helloworld-qt)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

if(CMAKE_VERSION VERSION_LESS "3.7.0")
    set(CMAKE_INCLUDE_CURRENT_DIR ON)
endif()

find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_executable(helloworld
    qt-main.cpp
)

target_link_libraries(helloworld Qt5::Widgets)
                      
                                              
