#------------------------------------------------------------------------------
#
# CMake build system for computability experiments
#
# > cmake -GNinja -DCMAKE_BUILD_TYPE=Release ..
#
#------------------------------------------------------------------------------
#
# This file is licensed after LGPL v3
# Look at: https://www.gnu.org/licenses/lgpl-3.0.en.html for details
#
#------------------------------------------------------------------------------

cmake_minimum_required(VERSION 3.15)
project(computability)
enable_testing()

add_library(frame INTERFACE)
target_include_directories(frame INTERFACE framework)

# library for drawing
add_subdirectory(drawer)

enable_testing()

# applications
add_subdirectory(apps)

install()