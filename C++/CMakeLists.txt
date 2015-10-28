cmake_minimum_required(VERSION 2.8)
set( CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} -std=c++0x)
project(fractals LANGUAGES CXX)

set( CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake/ )

find_package( SDL2 REQUIRED sdl2 )

include_directories(
    ${SDL2_INCLUDE_DIR}
)

add_executable(fractals graphics.cpp)
target_link_libraries(
    fractals
    ${SDL2_LIBRARY}
    pthread
)