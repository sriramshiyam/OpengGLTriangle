cmake_minimum_required(VERSION 3.0)
project(OpenGLDemo)
set(CMAKE_CXX_STANDARD 11)

find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(glm REQUIRED)

add_executable(OpenGLDemo)

target_include_directories(OpenGLDemo PRIVATE include)
file(GLOB_RECURSE SOURCE_FILES "src/*.cpp")

target_sources(OpenGLDemo PRIVATE ${SOURCE_FILES})

target_link_libraries(OpenGLDemo GLEW::GLEW glfw OpenGL::GL glm::glm)
