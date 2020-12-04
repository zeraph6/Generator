cmake_minimum_required(VERSION 3.17)
project(Generator)

set(CMAKE_CXX_STANDARD 14)

find_package(GSL REQUIRED)    # See below (2)

add_executable(Generator main.cpp)

target_link_libraries(Generator GSL::gsl GSL::gslcblas)