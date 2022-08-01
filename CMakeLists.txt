cmake_minimum_required(VERSION 3.23)
project(paspas)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS -O2)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)
find_package(Threads REQUIRED)

add_executable(paspas main.cpp)
target_link_libraries(paspas PRIVATE glfw vulkan Threads::Threads)
