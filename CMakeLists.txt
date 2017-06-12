project(opengles-a20)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. DIR_SRCS)
add_executable(opengles-a20 ${DIR_SRCS})

set (SRC_VERSION_MAJOR 1)
set (SRC_VERSION_MINOR 0)
set (SRC_VERSION_PATCH 1)
set (SRC_VERSION ${SRC_VERSION_MAJOR}.${SRC_VERSION_MINOR}.${SRC_VERSION_PATCH})
set (PROJECT_VERSION "${SRC_VERSION}")

add_definitions(-DLINUX)
add_definitions(-DEGL_API_FB)

target_link_libraries(opengles-a20 EGL)
target_link_libraries(opengles-a20 GLESv2)

install(TARGETS opengles-a20 DESTINATION bin)
