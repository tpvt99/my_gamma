cmake_minimum_required(VERSION 2.8)
project(GAMMA)

include(CTest)

set(CMAKE_CXX_STANDARD 17 CACHE STRING "C++ version selection")  # or 11, 14, 17, 20
set(CMAKE_CXX_STANDARD_REQUIRED ON)  # optional, ensure standard is supported
set(CMAKE_CXX_EXTENSIONS OFF)  # optional, keep compiler extensions off

set(CMAKE_CXX_FLAGS    " ${CMAKE_CXX_FLAGS_INIT} -std=c++17 -fPIC")

add_subdirectory(pybind11)
add_subdirectory(yaml-cpp)
add_subdirectory(src)
add_subdirectory(examples)


include(CPack)
