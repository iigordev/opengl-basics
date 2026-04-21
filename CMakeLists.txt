cmake_minimum_required(VERSION 3.20)
project(opengl-basics)

set(CMAKE_CXX_STANDARD 17)

include_directories(include)
link_directories(${CMAKE_CURRENT_SOURCE_DIR}/lib)

add_executable(opengl-basics main.cpp src/glad.c
        renderer.cpp
        renderer.h)

target_link_libraries(
        glfw3
        "-framework OpenGL"
        "-framework Cocoa"
        "-framework IOKit"
        "-framework CoreVideo"
)