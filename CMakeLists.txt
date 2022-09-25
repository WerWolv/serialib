project(serialib)
cmake_minimum_required(VERSION 2.9)

set(CMAKE_CXX_STANDARD 11)

option(SERIALIB_BUILD_EXAMPLES "Build serialib examples" OFF)
option(SERIALIB_BUILD_SHARED_LIBRARY "Build serialib as a shared library" OFF)

add_subdirectory(lib)

if (SERIALIB_BUILD_EXAMPLES)
    add_subdirectory(examples)
endif ()