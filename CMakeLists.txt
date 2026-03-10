cmake_minimum_required(VERSION 3.30)
project(netkit-server LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(netkit-server src/main.cpp)
find_package(netkit REQUIRED)

target_link_libraries(netkit-server PRIVATE netkit::netkit)
