cmake_minimum_required(VERSION 3.0)
project(OpenGL)

find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(OpenGL main.cpp)

target_link_libraries(OpenGL GLEW::GLEW glfw OpenGL::GL)
