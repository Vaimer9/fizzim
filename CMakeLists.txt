cmake_minimum_required(VERSION 3.22)

project(fizzim)
set(CMAKE_CXX_STANDARD 20)

set(SOURCES
    src/main.cpp
)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
include_directories(include)
add_executable(${PROJECT_NAME} ${SOURCES})

target_include_directories(${PROJECT_NAME} PUBLIC vendor)
add_subdirectory(vendor)
target_link_libraries(${PROJECT_NAME}
    PUBLIC SDL2 imgui)
