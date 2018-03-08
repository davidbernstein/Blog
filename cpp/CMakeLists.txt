# Authors: David Bernstein 

# cmake version
cmake_minimum_required(VERSION 3.9)

# project name
set(PROJECT_NAME DHB_BLOG_CPP)
project(${PROJECT_NAME})

# set cmake directory
#set(BLOG_CMAKE_DIR "${BLOG_SOURCE_DIR}/cmake" CACHE INTERNAL "")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# set build type
#set(CMAKE_BUILD_TYPE Release)
#set(CMAKE_BUILD_TYPE Debug)

# required packages


# c++ flags
set(CMAKE_CXX_STANDARD 17)

# library
add_library(blogLib "")
include(src/src.cmake)
target_include_directories(blogLib PUBLIC ${CMAKE_CURRENT_LIST_DIR})

# executable
add_executable(blog main.cpp)
target_include_directories(blog PUBLIC ${CMAKE_CURRENT_LIST_DIR})
target_link_libraries(blog blogLib)

