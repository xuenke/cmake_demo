cmake_minimum_required (VERSION 2.8)

project (demo3)

# 查找当前目录下所有源文件
# 并蒋名称保存到DIR_SRCS变量
aux_source_directory(. DIR_SRCS)

# 添加math子目录, 这使得math文件夹下的CMakeLists.txt和源码也会被处理
add_subdirectory(math)

# 指定生成目标
add_executable(demo main.cpp)

# 添加链接库,我们把math子目录中的文件单独编译，作为静态链接库添加到这里
# 注意：这里的math_functions是math子目录中编译生成的链接库的名称
target_link_libraries(demo math_functions)
