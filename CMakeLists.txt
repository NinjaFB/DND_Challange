cmake_minimum_required(VERSION 3.1)

project(DndChallenge)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED gtk4)

include_directories(${GTK4_INCLUDE_DIRS})
link_directories(${GTK4_LIBRARY_DIRS})

add_definitions(${GTK4_CFLAGS_OTHER})

add_executable(DndChallenge main.c)

target_link_libraries(DndChallenge ${GTK4_LIBRARIES})