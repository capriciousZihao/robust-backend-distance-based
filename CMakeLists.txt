# Cmake test file 

cmake_minimum_required(VERSION 2.6)
project(RRR)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake-modules/")
#下面这个设置是自己加的，为了支持c++11
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fPIC -ggdb")


find_package(G2O)
find_package(Eigen3)
find_package(SuiteSparse)

SET(CMAKE_BUILD_TYPE Release)
if("${CMAKE_BUILD_TYPE}" STREQUAL "")
  set(CMAKE_BUILD_TYPE Release)
endif()


add_subdirectory(examples)


