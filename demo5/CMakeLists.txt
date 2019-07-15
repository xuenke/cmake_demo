cmake_minimum_required (VERSION 2.8)

project(demo5)

# 这种方法能实现和demo3一样的构建效果，但是比demo3更为简洁
# 只需要定义一个CMakeLists.txt
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/math)

set(incs math/math_functions.h)

set(srcs math/math_functions.cpp)

add_executable(demo ${incs} ${srcs} main.cpp)
