cmake_minimum_required(VERSION 2.8)
project (nano3d)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

if (${CMAKE_CXX_COMPILER_ID} STREQUAL MSVC)
  message(STATUS "visual studio")
else()
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Wno-missing-braces -Wno-unused-function")
endif()

add_subdirectory(nano3d)
add_subdirectory(nano3d_ex)

add_subdirectory(tests)
add_subdirectory(examples)
