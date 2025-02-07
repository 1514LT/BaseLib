cmake_minimum_required(VERSION 3.12)
project(src)
set(CMAKE_CXX_STANDARD 11)
include_directories(${CMAKE_SOURCE_DIR}/../include)
# 添加动态库
add_library(Base SHARED
            Base.cpp
)

# 设置动态库和静态库的输出目录
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR})

if(DEFINED ARM64)
# 安装动态库和静态库
install(TARGETS Base 
        LIBRARY DESTINATION ${LIB_DIR}
)

else()
# 安装动态库和静态库
install(TARGETS Base 
        LIBRARY DESTINATION ${LIB_DIR}
)
endif()
