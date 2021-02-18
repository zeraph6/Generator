cmake_minimum_required(VERSION 3.17)
project(Generator)

#set(CMAKE_CXX_STANDARD 14)
set(CMAKE_C_STANDARD 11)

find_package(GSL REQUIRED)    # See below (2)

add_executable(Generator main.cpp)

target_link_libraries(Generator GSL::gsl GSL::gslcblas)

######Prog Args for query dataset
#--size
#100000
#--length
#256
#--z-normalize
#--filename
#"/home/zeraph/lernaean-hydra/DATA/queries_size100K_seed14784_len256_znorm.bin"