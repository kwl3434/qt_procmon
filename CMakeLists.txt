CMAKE_MINIMUM_REQUIRED(VERSION 3.5.0)

SET(proj_name "qt_procmon")
PROJECT( ${proj_name} )

# C++ settings
SET(CMAKE_CXX_STANDARD 14)

add_subdirectory(Src)
add_subdirectory(tests)
add_subdirectory(lib/googletest)
