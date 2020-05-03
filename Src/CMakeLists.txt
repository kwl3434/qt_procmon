#CMake Project name qt_procmon
project(qt_procmon)

#add_executable()    source file
#add_library()       library
#add_subdirectory()  directory path
#add_dependencies() dependencies

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

add_subdirectory(./helloworld/ 
	${CMAKE_RUNTIME_OUTPUT_DIRECTORY}
) 
