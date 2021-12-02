cmake_minimum_required(VERSION 3.12)

project(tree_sitter_cpp LANGUAGES C CXX ASM)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
set(BUILD_SHARED_LIBS ON)

include_directories(${PROJECT_SOURCE_DIR}/src)

file(GLOB_RECURSE
  SOURCE_FILES
    ${PROJECT_SOURCE_DIR}/src/*.c
    ${PROJECT_SOURCE_DIR}/src/*.cc
    ${PROJECT_SOURCE_DIR}/src/*.h
)

add_library(tree_sitter_cpp ${SOURCE_FILES})
