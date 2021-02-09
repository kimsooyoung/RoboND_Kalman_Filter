cmake_minimum_required(VERSION 3.0.0)
project(measurement_update VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(measurement_update main.cpp)
add_executable(solution solution.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
