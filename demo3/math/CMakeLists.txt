# 查找当前目录下所有源文件
# 并将变量名保存到DIR_LIB_SRCS变量
aux_source_directory(. DIR_LIB_SRCS)

# 生成链接库
add_library(math_functions ${DIR_LIB_SRCS})
