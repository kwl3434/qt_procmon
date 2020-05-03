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

IF(CMAKE_BUILD_TYPE MATCHES Debug)
  message("Debug build.")
ELSEIF(CMAKE_BUILD_TYPE MATCHES Release)
  message("Release build.")
ELSE()
  message("Some other build type.")
ENDIF()

if(LINUX)
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../build/Linux/x64_x86/${CMAKE_BUILD_TYPE} )
ELSEIF(WIN32)
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../build/Win/x32/${CMAKE_BUILD_TYPE} )
ELSEIF(WIN64)
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../build/Win/x64/${CMAKE_BUILD_TYPE} )

add_executable(helloworld
    qt-main.cpp
)

target_link_libraries(helloworld Qt5::Widgets)
                      
                                              
