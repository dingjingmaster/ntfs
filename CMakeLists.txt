cmake_minimum_required(VERSION 3.28)
project(ntfs)

set(CMAKE_CXX_STANDARD 11)

add_definitions(-DFUSE_USE_VERSION=26 -DHAVE_CONFIG_H)

add_subdirectory(app/ntfs-3g)
add_subdirectory(app/libntfs-3g)
add_subdirectory(app/libfuse-lite)

add_dependencies(ntfs-3g libntfs-3g libfuse-lite)
