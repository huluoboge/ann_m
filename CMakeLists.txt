cmake_minimum_required(VERSION 3.10)


project(ann_m C CXX)
 # guard against in-source builds
if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
    message(FATAL_ERROR "In-source builds not allowed.")
endif()

if(CMAKE_BUILD_TYPE)
    message(STATUS "Build type specified as ${CMAKE_BUILD_TYPE}")
else()
    message(STATUS "Build type not specified, using Release")
    set(CMAKE_BUILD_TYPE Release)
endif()

add_subdirectory(ANN)