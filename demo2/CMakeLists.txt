# 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目名称
project (demo2)

# 指定生成目标
add_executable(demo main.cpp math_functions.cpp)

# 如果我们写了很多源文件，有一个简单的办法把这个目录下所有源文件都加进来
# aux_source_directory(. DIR_SRCS)
# add_executable(demo ${DIR_SRCS})
