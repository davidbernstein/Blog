# Authors: David Bernstein 

# cmake version
cmake_minimum_required(VERSION 3.9)

# project name
set(PROJECT_NAME DHB_BLOG_CPP)
project(${PROJECT_NAME})

# set cmake directory
set(QBERT_COILY_CMAKE_DIR "${QBERT_COILY_SOURCE_DIR}/cmake" CACHE INTERNAL "")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# set build type
#set(CMAKE_BUILD_TYPE Release)
#set(CMAKE_BUILD_TYPE Debug)

# required packages


# c++ flags
set(CMAKE_CXX_STANDARD 17)

# add source
add_subdirectory(src)

