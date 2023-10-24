cmake_minimum_required(VERSION 3.26)
project(opengl_base)

set(CMAKE_CXX_STANDARD 17)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

# Add the GLFW source code directory to your project
add_subdirectory(external/glfw-3.3.8/)

add_executable(opengl_base main.cpp)

target_include_directories(opengl_base SYSTEM PUBLIC "external/glfw-3.3.8/include")

target_link_libraries(opengl_base PRIVATE glfw opengl32)