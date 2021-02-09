cmake_minimum_required(VERSION 3.0.0)
project(state_prediction VERSION 0.1.0)

# Mac os reqires this 
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include(CTest)
enable_testing()


add_executable(state_prediction main.cpp)
add_executable(solution solution.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
