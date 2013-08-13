cmake_minimum_required (VERSION 2.8)
project (swim)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PAH} "${CMAKE_SOURCE_DIR}/cmake/modules/")

find_package (OpenGL REQUIRED)
find_package (GLEW REQUIRED)
find_package (X11 REQUIRED)

include_directories(${OPENGL_INCLUDE_DIRS})
include_directories(${GLEW_INCLUDE_DIRS})
include_directories(${X11_INCLUDE_DIRS})

set (LIBS ${LIBS} ${OPENGL_LIBRARIES})
set (LIBS ${LIBS} ${GLEW_LIBRARIES})
set (LIBS ${LIBS} ${X11_LIBRARIES})

add_executable (swim main.cpp)

target_link_libraries (swim ${LIBS})
