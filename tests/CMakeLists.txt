
project(tests)

set(BINARY ${CMAKE_PROJECT_NAME}_tst)
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
#file(GLOB_RECURSE TEST_SOURCES LIST_DIRECTORIES false *.h *.cpp)

set(SOURCES ${TEST_SOURCES})


if(UNIX AND NOT APPLE)
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../build/Linux/x64_x86/${CMAKE_BUILD_TYPE} )
elseif("${CMAKE_SIZEOF_VOID_P}" EQUAL "8")
MESSAGE("++ 64 bit architecture")
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../Build/x64 )
set (CMAKE_PREFIX_PATH "C:\\Qt\\5.14.2\\msvc2017_64")
link_directories("../lib/googletest/lib/Release")
else(WIN32)
SET ( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../../Build/x86 )
set (CMAKE_PREFIX_PATH "C:\\Qt\\5.14.2\\msvc2017")
link_directories("../lib/googletest/lib/Release")
endif()


add_executable(${BINARY} main.cpp test1.cpp )
include_directories("../lib/googletest/googletest/include")
target_link_libraries(${BINARY} gtest)

add_test(NAME ${BINARY} COMMAND ${BINARY})


