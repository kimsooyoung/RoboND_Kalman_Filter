cmake_minimum_required(VERSION 3.0.0)
project(multi_dim_kf VERSION 0.1.0)

# Mac os reqires this 
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package (Eigen3 3.3 REQUIRED NO_MODULE)

include(CTest)
enable_testing()

add_executable(multi_dim_kf main.cpp)
add_executable(solution solution.cpp)
target_link_libraries (multi_dim_kf Eigen3::Eigen)
target_link_libraries (solution Eigen3::Eigen)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)


