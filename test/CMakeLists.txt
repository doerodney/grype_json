message("reading /test/CMakeLists.txt")

project(GrypeJsonTests LANGUAGES C CXX)

# Specify the C++ standard to use:
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Specify the C standard to use:
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

# Set the minimum version of cmake:
cmake_minimum_required(VERSION 3.0.0)

set(SOURCES main.cpp)

add_executable(json_grype_tests ${SOURCES})

target_include_directories(json_grype_tests PRIVATE ../src/include /usr/include/gtest)

target_link_libraries(json_grype_tests PRIVATE json_grype)
target_link_libraries(json_grype_tests PRIVATE gtest)
target_link_libraries(json_grype_tests PRIVATE pthread)
