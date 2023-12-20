cmake_minimum_required(VERSION 3.0)
project(OpenGL)
set(CMAKE_CXX_STANDARD 11)

find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(OpenGL)

target_include_directories(OpenGL PRIVATE include)
file(GLOB_RECURSE SOURCE_FILES "src/*.cpp")

target_sources(OpenGL PRIVATE ${SOURCE_FILES})

target_link_libraries(OpenGL GLEW::GLEW glfw OpenGL::GL)
