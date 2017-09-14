cmake_minimum_required(VERSION 3.7, FATAL_ERROR)
project(label_image)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES main.cpp)
add_executable(label_image ${SOURCE_FILES})

find_package(TensorflowCC COMPONENTS Shared)

target_link_libraries(label_image TensorflowCC::Shared)