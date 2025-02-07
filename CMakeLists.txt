cmake_minimum_required(VERSION 3.12)
project(Base)
set(INCLUDE_DIR ${CMAKE_SOURCE_DIR}/include)
if(DEFINED ARM64)
message(STATUS "target is arm64")
set(LIB_DIR ${CMAKE_SOURCE_DIR}/lib_arm64)
else()
message(STATUS "target is x86")
set(LIB_DIR ${CMAKE_SOURCE_DIR}/lib_x86)
endif()

add_subdirectory(src)
add_subdirectory(external)

