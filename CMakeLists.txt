cmake_minimum_required(VERSION 3.16)
project(shuys-util)
set(shuys-util_VERSION_MAJOR 0)
set(shuys-util_VERSION_MINOR 1)
set(shuys-util_VERSION_PATCH 0)

set(CMAKE_CXX_STANDARD 17)
set(CPP_STANDARD_COMPILE_FLAGS "-std=c++17")
set(OPTIMIZATION_FLAG_DEBUG "-O0")
set(OPTIMIZATION_FLAG_RELEASE "-Ofast")

set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS} ${OPTIMIZATION_FLAG_DEBUG}")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS} ${OPTIMIZATION_FLAG_RELEASE}")
add_definitions(${CPP_STANDARD_COMPILE_FLAGS})

include_directories("include/")

if (EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/tests/CMakeLists.txt")
    include(${CMAKE_CURRENT_SOURCE_DIR}/tests/CMakeLists.txt)
endif ()
