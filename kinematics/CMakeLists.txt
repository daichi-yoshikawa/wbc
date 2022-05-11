cmake_minimum_required(VERSION 3.10)

project(libkinematics
  VERSION 1.0.0
  DESCRIPTION "Robot Kinematics"
  LANGUAGES CXX)

set(EIGEN3_DIR CACHE STRING ../3rd_party/eigen-3.4.0/lib/share/eigen3)
find_package(Eigen3)
message(STATUS "EIGEN3 FOUND : ${Eigen3_FOUND}")
message(STATUS "INCLUDE DIRS : ${EIGEN3_INCLUDE_DIRS}")
message(STATUS "ROOT DIR : ${EIGEN3_ROOT_DIR}")

add_library(kinematics STATIC src/kinematics.cpp)
target_compile_features(kinematics PRIVATE cxx_std_20)
target_include_directories(kinematics PUBLIC ./include)

set_target_properties(kinematics
  PROPERTIES
  VERSION ${PROJECT_VERSION})
