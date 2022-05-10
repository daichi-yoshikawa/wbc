cmake_minimum_required(VERSION 3.10)

project(wbc
  VERSION 1.0.0
  DESCRIPTION "Whole Body Control Library"
  LANGUAGES CXX)

#set(CMAKE_CXX_STANDARD 20)
#set(CMAKE_CXX_STANDARD_REQUIRED True)

# STATIC, SHARED, or MODULE
# Or user may use options in compiling. -> BUILD_SHARED_LIBS(CMake cache variable)
#add_library(wbc STATIC ./src/wbc/kinematics.cpp)

# target_* commands require the following options.
# - PUBLIC : The command is for the target and anything depending on the target.
# - PRIVATE : The command is only for the target.
# - INTERFACE : The command is only for something depending on the target
# Eg. If main.cpp(executable main.o) includes my_lib.cpp(library my_lib.o), target and something depending on the target are my_lib and main respectively.
target_compile_features(wbc PRIVATE CXX_STD_11)
target_include_directories(wbc PUBLIC ./include)

set_target_properties(wbc PROPERTIES VERSION ${PROJECT_VERSION})



