cmake_minimum_required(VERSION 3.26)

set(This GoogleTestCPlusPlus)

project(${This} C CXX)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

enable_testing()

add_subdirectory(googletest)

set(Headers
    Testing.hpp
)

set(Sources
    Testing.cpp
)

add_library(${This} STATIC ${Sources} ${Headers})

add_subdirectory(test)

