cmake_minimum_required(VERSION 3.9)

# Second argument specifies what language
project(hello_world C)

# Use pkg-config to locate gtk4
find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED gtk4) 

include_directories(${GTK4_INCLUDE_DIRS})
message(status "GTK4_INCLUDE_DIRS = ${GTK4_INCLUDED_DIRS}")

link_directories(${GTK4_LIBRARY_DIRS})
message(status "GTK4_LIBRARY_DIRS = ${GTK4_LIBRARY_DIRS}")

add_definitions(${GTK4_CFLAGS_OTHER})
message(status "GTK4_CFLAGS_OTHER = ${GTK4_CFLAGS_OTHER}")

add_executable(hello_world main.c)

target_link_libraries(hello_world ${GTK4_LIBRARIES})
message(status "GTK4_LIBRARIES = ${GTK4_LIBRARIES}")

message(status "pkgs_cflags = ${PKGS_CFLAGS}")
