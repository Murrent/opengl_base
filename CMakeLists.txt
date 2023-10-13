cmake_minimum_required(VERSION 3.26)
project(opengl_base)

set(CMAKE_CXX_STANDARD 17)

# Add the GLFW source code directory to your project
add_subdirectory(external/glfw-3.3.8/)

add_executable(opengl_base main.cpp)

target_link_libraries(opengl_base PRIVATE glfw opengl32)