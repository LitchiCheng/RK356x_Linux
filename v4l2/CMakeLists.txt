cmake_minimum_required(VERSION 3.15)

set (CMAKE_C_COMPILER "aarch64-linux-gnu-gcc")
set (CMAKE_CXX_COMPILER "aarch64-linux-gnu-g++")

project(captureJpgApp)

add_executable(${PROJECT_NAME})
aux_source_directory(. sources)
aux_source_directory(tools sources)
target_sources(${PROJECT_NAME} PUBLIC ${sources})

target_include_directories(${PROJECT_NAME} PUBLIC
                           ../utility
                           tools
                           )