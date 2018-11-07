cmake_minimum_required(VERSION 3.9)
project(Lab_3 C)

set(CMAKE_C_STANDARD 99)

set(MY_STR_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/my_str)

add_subdirectory(my_str)

include_directories($(MY_STR_INCLUDE_DIR))

add_executable(example example.c)

target_link_libraries(example lib_string)
ADD_DEPENDENCIES(example lib_string)


