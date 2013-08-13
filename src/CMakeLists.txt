cmake_minimum_required (VERSION 2.8)
project (swim)


find_package (OpenGL)
find_package (GLEW)

add_executable (swim main.cpp)

target_link_libraries (swim ${OPENGL_LIBRARIES} ${GLEW_LIBRARIES})
