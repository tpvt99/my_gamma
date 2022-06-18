cmake_minimum_required(VERSION 2.8)
project(GAMMA)

include(CTest)


set(CMAKE_CXX_FLAGS    " ${CMAKE_CXX_FLAGS_INIT} -std=c++11 -fPIC")

add_subdirectory(pybind11)

add_subdirectory(src)
add_subdirectory(examples)

include(CPack)
