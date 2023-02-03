cmake_minimum_required(VERSION 3.24)
project(hello_gtk C)

set(CMAKE_C_STANDARD 23)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED gtk4)

include_directories(${GTK4_INCLUDE_DIRS})
link_directories(${GTK4_LIBRARY_DIRS})


add_executable(hello_gtk main.c)
target_link_libraries(hello_gtk ${GTK4_LIBRARIES})
