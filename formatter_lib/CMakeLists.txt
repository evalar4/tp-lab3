cmake_minimum_required(VERSION 3.10)

project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(SOURCES
    formatter.cpp
)

add_library(formatter STATIC ${SOURCES})

target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

