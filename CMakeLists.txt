cmake_minimum_required(VERSION 2.8)

# project information
project(liblsoda C CXX)

# cmake modules
include(CMakeCXXInformation)
include(CheckCXXCompilerFlag)

# build type
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release CACHE STRING
    "Choose the type of build, options are: None Debug Release RelWithDebInfo MinSizeRel."
    FORCE)
endif(NOT CMAKE_BUILD_TYPE)

# variables
set(CMAKE_MACOSX_RPATH 1)
set(LIBLSODA_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/src)

add_subdirectory(src)
add_subdirectory(test)
