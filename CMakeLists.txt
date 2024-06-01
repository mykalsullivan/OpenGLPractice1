cmake_minimum_required(VERSION 3.28)
project(OpenGLPractice1)

set(CMAKE_CXX_STANDARD 23)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

add_executable(OpenGLPractice1
        src/main.cpp
)

include_directories(
        ${OPENGL_INCLUDE_DIRS}
        ${GLUT_INCLUDE_DIRS}
)

target_link_libraries(OpenGLPractice1
        glfw
        ${OPENGL_LIBRARIES}
        GLEW
)