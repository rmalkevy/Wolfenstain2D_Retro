cmake_minimum_required(VERSION 3.8)
project(Wolf)

set(CMAKE_C_STANDARD 99)

include_directories(inc includes minilibx)
link_directories(minilibx)

set(SOURCE_FILES main.c wolf.h)
add_executable(Wolf ${SOURCE_FILES})

target_link_libraries(Wolf libmlx.a "-framework OpenGL" "-framework AppKit")